---
id: intro
title: Introduction to Parsers
sidebar_label: What are parsers?
---

EventBridge Atlas is a tool to help engineers discover, document and explore AWS Event Schemas.

There are many ways in which engineers may choose to document their Events, and EventBridge Atlas allows engineers to select which output they desire.

EventBridge Atlas Parsers allows us to generate desired outputs using the same AWS inputs.

## How it works

![Events](/img/docs/how-it-works/architecture-2.png 'Architecture')

Parsers are build up in three stages

- Init
- Build
- Wrapup (optional)

##### Init Stage

The init stage of the parser is used to generate the required format for the 3rd party tools.

For example, the init stage of the `docuowl` parser, will generate the required markdown files needed for docuowl.

##### Build Stage

The build stage of the parser is used to use the 3rd party tool to generate the documentation and output (HTML).

For example, the build stage of the `docuowl` parser will run your markdown files through `docuowl` to give you documentation!

##### Wrapup (optional)

The wrapup stage is called and used to wrap up what ever you want, maybe extra tidy up on files, or mutations to output files from the 3rd party tools.

## Building your own Parser

There is work to do here, but if you would like to experiment and build your own parser take a look at how the parsers we have are working. You can find the parsers in `src/parsers`.

> If your interested and/or stuck please reach out and I'm more than happy to help and support and improve the API when required.
