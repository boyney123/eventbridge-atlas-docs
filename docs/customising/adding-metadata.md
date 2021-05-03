---
id: adding-metadata
title: Adding metadata to schema
sidebar_label: Adding metadata to schema
---

**EventBridge Atlas** allows us to add extra information onto your event schemas!

You can:

- Add example events for each event
- Add descriptions to each event source
- Add descriptions per property on your events

The magic happens in `/data/event-metadata.json`.

> Once you are done editing the event-metadata.json file, you have to rebuild the docs.

###### Example event-metadata.json

```js
{
  "yourevent.source": {  // name of each source
    "metadata": {
      "title": "Some general description for this event source" // description for your source
    },
    "events": {
      "UserCreated": { // This is your Event (UserCreated, UserDeleted, etc. Make sure they match)
        "description": "Event is raised when the user is created.", // Description for event
        "properties": {
          "name": "The name of the user that was just created", // Document each property!
          "email": "The email of the customer" // Another example of documenting the email property. Add as many as you like.
        },
        "example": { // This is a JSON example of your event in action.
          "version": "100",
          "id": "5d57eb17-c910-b2de-3996-6b98c5f60dbc",
          "detail-type": "UserCreated",
          "source": "yourevent.source",
          "account": "764738355555",
          "time": "2021-03-12T12:53:38Z",
          "region": "eu-west-1",
          "resources": [],
          "detail": {
            "data": {
              "name": "Dave",
              "email": "dave@boyney.io"
            }
          }
        }
      }
    }
  }
}
```

Let's look at how you can get that working.

#### Add example events for each event

Open up the `/data/event-metadata.json` file and you should see an example.

Any Event you add documentation for you can add an example of the event.

As seen in our example below, any JSON payload against the `example` property will be rendered on screen.

###### Example event-metadata.json

```js
{
  "myApp.users": {
    ...
    "events": {
      "UserCreated": {
        ...
        "example": { // This is a JSON example of your event in action. Replace this with your example!
          "version": "100",
          "id": "5d57eb17-c910-b2de-3996-6b98c5f60dbc",
          "detail-type": "UserCreated",
          "source": "yourevent.source",
          "account": "764738355555",
          "time": "2021-03-12T12:53:38Z",
          "region": "eu-west-1",
          "resources": [],
          "detail": {
            "data": {
              "name": "Dave",
              "email": "dave@boyney.io"
            }
          }
        }
      }
    }
  }
}
```

###### Example of what your event example will look like (using the docuowl parser)

![Events](/img/docs/adding-metadata/example.png 'Example of Example :)')

#### Add descriptions to each event source

Open up the `/data/event-metadata.json` file.

```js
{
  "myApp.users": {  // name of each event source
    "metadata": {
      "title": "Some general description for this event source" // description for your source here!
    },
    ...
  }
}

```

Just update the `title` as seen above and the description will be rendered below your event source as seen in the photo below.

![Events](/img/docs/adding-metadata/event-source.png 'Example of event source details')

###### Add descriptions per property on your events

For every event you can write descriptions for each property on the event!

Open up the `/data/event-metadata.json` file.

```js
{
  "myApp.user": {
   ...
    "events": {
      "UserCreated": {
        ...
        "properties": {
          "name": "The name of the user that was just created", // Description for the property `name`
          "email": "The email of the customer" // Description for the property `email`
        },
        ...
    }
  }
}
```

![Events](/img/docs/adding-metadata/property.png 'Example of event property details')

#### Adding more...

If you have any ideas or want more please feel free to raise an issue or get in touch. I started with these basic ones, but no doubt I missed some great use cases!
