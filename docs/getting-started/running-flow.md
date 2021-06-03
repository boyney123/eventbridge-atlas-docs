---
id: running-flow
title: Running with Flow (node diagram)
sidebar_label: Running with flow (node diagram)
---

#### Outputting flow (node diagram) Docs

![Flow](/img/docs/parsers/flow-example.png 'Flow Example')

To run the application you will need to run

```javascript
npm run build:flow
```

This will download the required information from AWS and run your data through the `flow` parser.

The parser will generate the documentation for you. Simple!

After this process is complete you can run this next command to start the server on your machine.

```javascript
npm run start-server -- docs-html/flow
```

That's it!

> Remember to have your .env file setup. If you run into any problems feel free to reach out.

### Customise your data and events

Now (hopefully) you should have your events displayed and documented! Awesome.

Now you can customise your events further, read [customising events](/docs/customising/adding-metadata).
