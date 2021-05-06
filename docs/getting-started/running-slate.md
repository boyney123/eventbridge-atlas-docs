---
id: running-slate
title: Running with Slate
sidebar_label: Running with slate
---

#### Outputting Slate Docs

![slate](/img/docs/parsers/slate-example.png 'slate Example')

To run the application you will need to run

```javascript
npm run build:slate
```

This will download the required information from AWS and run your data through the `slate` parser.

After this process is complete you can run this next command to start the server on your machine.

```javascript
npm run start-server -- docs-html/slate
```

That's it!

> Remember to have your .env file setup. If you run into any problems feel free to reach out.

### Customise your data and events

Now (hopefully) you should have your events displayed and documented! Awesome.

Now you can customise your events further, read [customising events](/docs/customising/adding-metadata).
