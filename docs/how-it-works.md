---
id: how-it-works
title: How it works
sidebar_label: How it works
---

![Events](/img/docs/how-it-works/architecture-2.png 'Architecture')

**EventBridge Atlas** is quite simple under the hood. It just merges a few tools together and generates documentation for our schemas.

You could split **EventBridge Atlas** into these parts.

1. AWS Integration (Fetching data from AWS)
2. Running the Parser (Generating the docs using tools)
3. HTML Output (Hosting the output)

#### 1. AWS Integration

When you start the application it will require access to your AWS account (.env file).

The `aws-sdk` is used to fetch:

- Your schemas
- Information about your Registry and Eventbus
- Information about the Targets (subscribers) for your events

> You will need to turn Event Discovery on for this application. But more on this later.

EventBridge Atlas is built around its `parsers`, these are the scripts used to generate your documentation into the format you wish.

So once we have the information we need from AWS, EventBridge Atlas with take your chosen `format` and generate documentation for it.

#### 2. Running the Parser

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

#### Support parsers are the moment:

- [docuowl](https://github.com/docuowl/docuowl)
- [asyncapi](https://www.asyncapi.com/)

#### 3. HTML Output

Each parser will generate static HTML which is great. You can run this locally using our commands (more on this later), or host wherever you like.
