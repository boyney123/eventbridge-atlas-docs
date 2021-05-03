---
id: running-docuowl
title: Running with Docuowl
sidebar_label: Running with docuowl
---

#### Outputting Docuowl Docs

![Docuowl](/img/docs/parsers/docuowl-example.png 'Docuowl Example')

To run the application you will need to run

```javascript
npm run build:docuowl
```

This will download the required information from AWS and run your data through the `docuowl` parser.

The parser will generate the documentation for you. Simple!

After this process is complete you can run this next command to start the server on your machine.

```javascript
npm run start-server -- docs-html/docuowl
```

That's it!

> Remember to have your .env file setup. If you run into any problems feel free to reach out.

### Customise your data and events

Now (hopefully) you should have your events displayed and documented! Awesome.

Now you can customise your events further, read [customising events](/docs/customising/adding-metadata).
