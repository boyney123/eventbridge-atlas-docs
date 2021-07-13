---
id: populate-eventmetadata
title: Populating your Event Metdata
sidebar_label: Populating your Event Metdata
---

To get the most out of EventBridge Atlas, we recommended you take advantage of the **metadata** feature.

This allows you to provide descriptions for your Event detail properties and also examples.

##### Getting Started

Populating data takes seconds, just run the following command:

```bash
npm run generate-eventmetadata
```

This will generate folders within your `/data` directory. Each folder will contain the `source` and `event`.

For example you will see `/data/{event-source}/{detailType}.json`.

Within this file you will see properties you can add descriptions too and also the example payload.

##### Example

Here is an example of what will be generated for you

```js
{
    "description": "My Event is raised when our system does something interested. Change this to what you want.",
    "detail": {
        "brand": {
            "code": {
                "type": "string",
                "description": "The brand of the user", // Fill out the details for each description. The template is made for you
                "example": ""
            }
        },
        "data": {
            "applicationProductIds": {
                "type": "array",
                "description": "",
                "example": ""
            },
            "decision": {
                "type": "string",
                "description": "",
                "example": ""
            },
            "decision_at": {
                "type": "string",
                "description": "",
                "example": ""
            },
            "status": {
                "type": "string",
                "description": "",
                "example": ""
            }
        },
        "metadata": {
            "correlationId": {
                "type": "string",
                "description": "",
                "example": ""
            },
            "service": {
                "type": "string",
                "description": "",
                "example": ""
            }
        },
        "user": {
            "id": {
                "type": "number",
                "description": "",
                "example": ""
            }
        }
    },
    "example": { // This example is prepopulated for you. Just change the defaults.
        "detail-type": "MyEvent",
        "resources": [],
        "detail": {
            "metadata": {
                "service": "ut",
                "correlationId": "sed eiusmod"
            },
            "data": {
                "decision": "sit deserunt officia incididunt sint",
                "decision_at": "1999-04-13T23:00:00.0Z",
                "brand": {
                    "code": "magna deserunt ex sit exercitation"
                },
                "user": {
                    "id": 1
                },
                "applicationProductIds": [1, 2, 3],
                "status": "active"
            }
        },
        "id": "29a3717a-3304-423e-9595-46c020ab33d8",
        "source": "deadhappy.claims",
        "time": "2021-07-13T06:51:53.741Z",
        "region": "eu-west-1",
        "version": "4",
        "account": "YOUR_ACCOUNT"
    }
}
```


