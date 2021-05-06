---
id: setup
title: Setup
sidebar_label: Setup
---

In order to get **EventBridge Atlas** setup and running you will need to fill in the .env file.

### .env file

You should see `.env-example` in the directory. Rename this to `.env`.

Your env file will look something like this

```bash

# The name of your custom event bus. Used to get the rules for each event on your bus.
EVENT_BUS_NAME=

# Your schema registry name. (Discovered Schema Registry name. Continue to read docs to see how you can set this up)
SCHEMA_REGISTRY_NAME=

# Region the event bus is in
REGION=

# AWS ACCESS KEY
AWS_ACCESS_KEY_ID=

# AWS SECRET KEY
AWS_SECRET_ACCESS_KEY=

# AWS SESSION TOKEN
AWS_SESSION_TOKEN=

```

> Hopefully most things in the .env are understandable, but if you are struggling feel free to reach out or leave a comment on the GitHub repo and I will add more information to help people.

Now you have setup your `.env` file we are good to go.

### Running the application

EventBridge Atlas allow you to select which format you would like to generate your docs with.

Continue reading to get started with the `slate` output.
