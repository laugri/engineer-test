# Context

As the most senior engineer in your squad, you work in a fast-paced environment where quality software delivery must be balanced with rapidly evolving product needs.
You are integrating a new API from an existing ERP so that this ERPs' customers can use our product.

## Step 1: Web API

We first need to be able to query **unassigned visits**. Two fields are available for queries:

- Agency name
- Date

You already have access to a third-party API (mocked and represented by the file `visits.json`) listing all visits, and you are going to build a wrapper around it.

A visit is _unassigned_ if:

- its start date is in the future
- it has no assigned worker

Here is the payload you should obtain when querying unassigned visits for the Paris agency:

```json
[
  {
    "description": "Evening meal assistance - Mrs. Bernard",
    "start_date": "2025-06-16T18:00:00",
    "end_date": "2025-06-16T19:00:00",
    "agency": "Paris",
    "worker": null
  }
]
```

## Step 2: Command-line interface

You will then build a command-line interface that displays the list of unassigned visits for a given agency. You already have access to the file `agencies.json` that maps agency codes to agency names. You will leverage what you have already built in the previous step.

Here is the output you should get for the country code "PAR":

```txt
Evening meal assistance - Mrs. Bernard, Paris
```

# Instructions

- [ ] Clone this repository (do **not** fork it)
- [ ] Implement the features step-by-step (your commit history should be clear to follow)
- [ ] Document & explain your architecture and design choices along the way
- [ ] Provide clear instructions on how we can run your code
- [ ] Publish it on GitHub (or equivalent)
- [ ] Send us the link, along with an estimate of how much time you spent on this assignment

## Guidelines

### Starting pack

To get you started quicker, we setup a typescript monorepo with an API and a CLI.

### Choose your stack

We provide a starter TypeScript monorepo (including a basic API and CLI setup), but you’re free to use any language, framework, or toolset you're comfortable with.
You may structure the project however you like, monolith or modular, layered or flat, as long as your design decisions are clearly explained.
Feel free to use open-source libraries to support your solution where it makes sense.

Example stack (not limited to): http server exposing REST endpoint that serves json payloads.

### Assumptions

If anything is unclear, you can make reasonable assumptions and document them

### Use of AI is allowed

Feel free to use AI like you would in your daily work.

### Time management

Usually, this assignment is completed within 3-4 hours.
Please limit your time to 3 hours maximum on this assignment.

## Expectations

- [ ] You followed the instructions
- [ ] Your architecture and design choices are clearly documented
- [ ] The Web API is functional and queryable
- [ ] The CLI tool runs as expected
- [ ] Tests are included and runnable
- [ ] There is a clear separation of concerns
  - _e.g., keep core logic well isolated_
  - _you can apply DDD patterns if you are familiar with them like meaningful entities and clear layers_
- [ ] The application is free of bugs

## Out of scope

- Authentication / authorization
- Usage of third party tools, like a CI service
- Performance
- Security

# Setup instructions

In order to setup and run the existing basic project we provided:

- install node (see .nvmrc)
- install and run `pnpm install`
- Refer to the README files in the `packages/api` and `packages/cli` directories for additional details

# Final Thoughts

Let us know if you have any questions or blockers. We're evaluating your reasoning and clarity as much as your code. Explain your decisions and trade-offs like you would in a real-world setting.
