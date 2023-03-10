> We were not accepted into GSoC 2023. We still offer regular internship, but not in the same format.

# GSoC 2023 Ideas List

Welcome! If you haven't read the [GSoC Contributing Guide](CONTRIBUTING.md) please read it first before going through the ideas list.

Prospective contributors, please open a discussion with us on [Discussions](https://github.com/SeaQL/summer-of-code/discussions)!

## 1. Expand the features of [SeaORM](https://github.com/SeaQL/sea-orm) - An async & dynamic ORM for Rust

SeaORM is the flagship project of SeaQL. We run a fast iteration cycle, now approaching our 11th release. We have set a solid [architecture](https://www.sea-ql.org/SeaORM/docs/internal-design/architecture/) for expanding the usefulness of an ORM in building data-driven applications, but there is still more to be desired. During this Summer of Code project, you will be involved in one full release cycle and go through it from design to delivery. SeaORM is a maturing project, so the experience will be different from a greenfield "from scratch" project. But we assure the process will be as much fun and much more impactful. Here is an outline of the process:

1. Ideation. Draft and refine several ["Proposal & Implementation Plan" (PIP)](https://github.com/SeaQL/sea-orm/issues?q=is%3Aissue+%5BPIP%5D)s
2. Implementation. Implement the feature following our [Engineering Practices](https://www.sea-ql.org/blog/2022-07-30-engineering/)
3. Review. Solicit reviews and improve upon the implementation following our [Review Guidelines](https://www.sea-ql.org/blog/2023-01-01-call-for-contributors-n-reviewers/#what-are-the-criteria-when-reviewing-a-pr)
4. Documentation. Write throughout documentation and may be tutorials to guide users of the new feature
5. Release. Co-author the release notes and make an announcement
6. Reception. Gather user feedback and summarize on possible improvements

Tips for drafting a proposal: it is important to have had first-hand experience using SeaORM. Identify one or more aspects you want to improve, and focus on them. Here are several suggestions, but feel free to come up with yours. Include no more than 3 major features in your proposal.

1. Event stream: https://github.com/SeaQL/sea-orm/issues/1123
2. Schema compatibility check: https://github.com/SeaQL/sea-orm/issues/1122
3. Soft delete: https://github.com/SeaQL/sea-orm/issues/220

**Deliverables:** 1, 2 or at most 3 major features in a SeaORM release

**Skills Required:**

- Hands on experience with SeaORM
- Solid knowledge in Rust and SQL

**Possible Mentors:**

- [Chris Tsang](https://github.com/tyt2y3)
- [Billy Chan](https://github.com/billy1624)
- [Sanford Pun](https://github.com/shpun817)

**Expected Size of Project:** 350 hours

**Difficulty Rating of Project:** Medium

## 2. Expand the features of [Seaography](https://github.com/SeaQL/seaography) - A GraphQL framework for SeaORM

We would like to continue improve upon this project and here are several areas:

1. GraphQL Mutation. CRUD on a single entity is pretty straight forward, but we need to think about to what extend we implement nested insert/update, and especially has to watch out on delete propagation and orphans. We should NOT attempt to cater the most generic M-N recursive graphical schema, but can cater for constrained cases like a tree with limited depth. We should also make the framework flexible enough to allow users to plug in their own mutation logic

2. GraphQL Access Control. With mutation, naturally we need access control otherwise anyone will be able to change anything. We can implement [Role-based access control](https://en.wikipedia.org/wiki/Role-based_access_control) in database separate from the data store database. The bigger question though, is how we assert that on individual queries. Just to skim over the problem, there are several granularity of access: per entity (table), field (column) and record (row). For example, we can easily reject a query when it touches an entity that the user is not allowed to access anywhere in the query tree. In some cases, we only want to redact certain fields (say the password field of User). In addition, we might want to restrict access to a subset of records. This is useful in, say, a User is only allowed to access objects *where they are the owner*. 

    + Apollo made a great discussion on this complex subject matter: https://www.apollographql.com/blog/backend/auth/authorization-in-graphql/

3. GraphQL Subscriptions. This depends on a supporting feature of SeaORM: https://github.com/SeaQL/sea-orm/issues/1123 , so if you include this in your project, you will also have to take up the responsibility to work on SeaORM

This endeavor is likely going to also require improvements on upstream projects: namely SeaORM and [async-graphql](https://github.com/async-graphql/async-graphql), so familiarize yourself with them too.

**Deliverables:** A milestone release of Seaography with 1, 2 or at most 3 major features

**Skills Required:**

- Hands on experience with GraphQL
- Solid knowledge in Rust and SQL

**Possible Mentors:**

- [Chris Tsang](https://github.com/tyt2y3)
- [Billy Chan](https://github.com/billy1624)
- [Sanford Pun](https://github.com/shpun817)

**Expected Size of Project:** 350 hours

**Difficulty Rating of Project:** Hard

## 3. Continue working on [OtterSQL](https://github.com/SeaQL/otter-sql) - An Embeddable SQL Executor

Well, we are growing our own SQL implementation? It is extremely preliminary for now, so the project will likely undergo significant architectural changes, but the foundation and basic ideas are set. In reality, it will take years for this to become production-ready, but it will be useful enough to implement a subset of SQL that SeaORM actually uses, which, is plausibly doable.

This is by far the most academic / research oriented project. Go for this project if you want to be more theoretical.

**Deliverables:** A milestone release of OtterSQL with significant improvements

**Skills Required:**

- Solid knowledge in Rust and SQL
- Interest and knowledge in programming languages and compilers

**Possible Mentors:**

- [Chris Tsang](https://github.com/tyt2y3)
- [Billy Chan](https://github.com/billy1624)
- [Sanford Pun](https://github.com/shpun817)

**Expected Size of Project:** 350 hours

**Difficulty Rating of Project:** Hard

## 4. A media-centric CMS based on SeaORM & Seaography

Think "WordPress but for images and short videos". The goals of this project are:

1. To demonstrate the usefulness of the Rust / SeaQL ecosystem with an open-source, real-world project
2. To identify areas of improvements to the ecosystem while developing it
3. To be a useful product allowing users to self-host it

Frontend skills is needed, but the focus is on the backend, so it's okay to deliver a minimal UI.

To limit the scope of the project, here are some restrictions:

1. Everything is public, and there is no user registration
2. There will be no admin panel. So there is only one user-facing API and GUI
3. There will be only one mobile-first pre-compiled SPA, so don't spend time on SSR or things like that
4. The frontend will interface with the backend via GraphQL, and there is no mutation
5. The frontend must be either Vue or React and based on a framework like Nuxt.js or Next.js etc

If there is no admin panel, how does the CMS work? File system. Basically we want to design a reasonable directory format and glorify it. All metadata will be stored in the `toml` file format, so it might actually look like a `Cargo` file.

Admin simply have to ssh into the server and upload some files and viola! It will also be very easy to deploy - just run the binary. To provide a good experience, it is important that we listen to file system events and update the database index immediately. https://github.com/emcrisostomo/fswatch is a great library and there is a Rust binding too https://github.com/ascclemens/fswatch-sys (we might need to update its dependency).

We will need a database to store the metadata, but the source of truth is the file system. We can use SQLite as the datastore, so there will be no external dependency. We need to be able to update the metadata database incrementally, i.e. if we updated a sub-directory, we only want to update the corresponding subset of the database.

Finally, reaction (like and other emoji) and comments will be a bonus feature, if we have time.

Note: just like WordPress, this project is likely to be GPL licensed. All other SeaQL projects up to now are MIT.

**Deliverables:** An initial release of the product

**Skills Required:**

- Solid knowledge in Rust
- Experience with SeaORM and Seaography
- Experience in frontend development

**Possible Mentors:**

- [Chris Tsang](https://github.com/tyt2y3)
- [Billy Chan](https://github.com/billy1624)
- [Sanford Pun](https://github.com/shpun817)

**Expected Size of Project:** 350 hours

**Difficulty Rating of Project:** Medium

## 5. A MongoDB-like query pipeline implementation

This project will serve as the foundation for an upcoming document-oriented data processing library. Think of it like an ORM for MongoDB. At SeaQL, we like to be able to simulate everything in a miniaturized fashion - i.e. you can replace MySQL with SQLite in SeaORM. It will be great to have a pure Rust implementation of the logic layer of MongoDB!

Luckily, there is already a great example of such implementation - https://github.com/kofrasa/mingo, so there is a lot to learn from there. It will be a good start to port this library to Rust, and gradually refactor / re-architect it to be [idiomatic Rust](https://github.com/mre/idiomatic-rust).

**Deliverables:** An initial release of the library, with plenty of tests

**Skills Required:**

- Solid knowledge in Rust and TypeScript
- Experience with MongoDB

**Possible Mentors:**

- [Chris Tsang](https://github.com/tyt2y3)
- [Billy Chan](https://github.com/billy1624)
- [Sanford Pun](https://github.com/shpun817)

**Expected Size of Project:** 350 hours

**Difficulty Rating of Project:** Medium
