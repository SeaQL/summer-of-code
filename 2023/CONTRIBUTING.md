# GSoC 2023 with SeaQL

[GSoC 2023 Organization Profile](https://summerofcode.withgoogle.com/programs/2023/organizations/seaql)

First of all, thank you for your interest in SeaQL and the intention to contribute.

## About SeaQL

In 2020, when we were developing systems in Rust, we noticed a missing piece in the ecosystem: an ORM that integrates well with the Rust async ecosystem.

The first piece of tool we released is [SeaQuery](https://github.com/SeaQL/sea-query), a query builder with a fluent API. It has a simplified AST that reflects SQL syntax. It frees you from stitching strings together in case you needed to construct SQL dynamically and safely, with the advantages of Rust typings.

The second piece of tool is [SeaSchema](https://github.com/SeaQL/sea-schema), a schema manager that allows you to discover and manipulate database schema. The type definition of the schema is database-specific and thus reflecting the features of MySQL, Postgres and SQLite tightly. It has been the backbone of the awesome SeaORM / Seaography Codegen.

The third piece of tool is [SeaORM](https://github.com/SeaQL/sea-orm), an Object Relational Mapper for building web services in Rust, whether it's REST, gRPC or GraphQL. We always have "async & dynamic" in mind, so developers from dynamic languages can feel right at home.

The forth piece of tool is [Seaography](https://github.com/SeaQL/seaography), a GraphQL framework for SeaORM. It helps you to spin up a basic GraphQL server in minutes! Arguably this is the killer feature of the SeaQL ecosystem where the power of async & dynamic truly shines.

## Before you apply

Make sure you read everything on https://google.github.io/gsocguides/student/ and "Internship @ SeaQL".

On top of that, there are a few points we'd want you to know:

1. GSoC is not (just) an internship. It's a privilege to be paid for open source contribution. So you have to put in 120% effort and compete for that privilege. You must have no other commitment during the project period.

2. Since the mode of work is fully-remote and async (as we will likely spread across different timezones), discipline and prompt communication is required. And please, listen to your mentors. We have failed contributors in the past because of these reasons.

3. Familiarity with the Rust language and the ecosystem is a must. The designs of SeaQL's projects are based on Rust's unique features and those are what makes SeaQL unique.

## How to apply

1. [Contribute to an existing project](#contribute-to-an-existing-project)
2. [Choose a GSoC Project](#choose-a-gsoc-project)
3. [Submit Your Application](#submit-your-application)

## Contribute to an existing project

We want our new contributors to be familiar with Rust and our projects. Please make at least one contribution to the project mentioned above on GitHub.

There are many forms of contributions:

 + Submitting pull request for an issue to implement a new feature or fix a bug. You might want to take on issue with "good first issue" label. We've got your back! You can always open an draft pull request and ask for help on GitHub or Discord.
 + Suggesting a new feature by filing an issue if you have any insightful ideas
 + Reviewing pull request if you are comfortable with the source code and want to peek into new features
 + Commenting on existing issue if you want to share your thoughts on it

## Choose a GSoC Project

We have composed a [GSoC project ideas list](README.md) for you to choose from. You can contact us through one of the channel listed below, introduce yourself and suggest your own project ideas before submitting your application. Feel free to chat with us if you have any questions or thoughts on the project idea.

## Submit Your Application

> TBC

## How to Find Us?

You can ask questions or talk to us by:

 + Opening a [GitHub Discussions](https://github.com/SeaQL/summer-of-code/discussions)
 + Chatting with us on [Discord server](https://discord.com/invite/uCPdDXzbdv)