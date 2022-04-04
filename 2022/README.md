# GSoC 2022 Ideas List

Welcome! If you haven't read the [GSoC Contributing Guide](CONTRIBUTING.md) please read it first before going through the ideas list.

Prospective contributors, please open a discussion with us on [Discussions](https://github.com/SeaQL/summer-of-code/discussions)!

## 1. A GraphQL framework on top of SeaORM

We would like to have a GraphQL framework / engine that build's on top of SeaORM. It is now doable to roll your own GraphQL solution using SeaORM, but it is so cumbersome and every resolver has to be coded by hand. We could take inspiration from [awto](https://github.com/awto-rs/awto), where database schema follows a set convention, so that we are able to provide common GraphQL operations (pagination, filtering, sorting, joining etc) out-of-the-box. We can also take inspiration from Hasura or Dgraph of developing a GraphQL engine. The exact approach has to be discussed, as we do not want to duplicate Hasura, which is itself a pretty great open source project.

**Deliverables:** An extensible and customizable GraphQL framework / engine works on top of SeaORM

**Skills Preferred:**

- Knowledge in GraphQL
- Experience in Rust & SQL

**Possible Mentors:**

- [Chris Tsang](https://github.com/tyt2y3)
- [Billy Chan](https://github.com/billy1624)
- [Sanford Pun](https://github.com/shpun817)

**Expected Size of Project:** 350 hours

**Difficulty Rating of Project:** Medium

**Reference:**

- [Wrap a REST API with GraphQL - A 3-step tutorial | Prisma](https://www.prisma.io/blog/how-to-wrap-a-rest-api-with-graphql-8bf3fb17547d)
- [GraphQL Search and Filter &ndash; How to search and filter results with GraphQL - Apollo GraphQL Blog](https://www.apollographql.com/blog/graphql/filtering/how-to-search-and-filter-results-with-graphql/)
- [GraphQL relationships | Fauna Documentation](https://docs.fauna.com/fauna/current/api/graphql/relationships)
- [Queries and Mutations | GraphQL](https://graphql.org/learn/queries/)
- [Search and Filtering - GraphQL (dgraph.io)](https://dgraph.io/docs/graphql/queries/search-filtering/#filter-a-query-for-a-range-of-objects-with-between)
- [GraphQL in Rust | Roman Kudryashov&#39;s tech blog](https://romankudryashov.com/blog/2020/12/graphql-rust/)
- [Building a GraphQL to SQL Compiler on Postgres, MS SQL, and MySQL (hasura.io)](https://hasura.io/blog/building-a-graphql-to-sql-compiler-on-postgres-ms-sql-and-mysql/)
- [Postgres: Filter query results / search queries | Hasura GraphQL Docs](https://hasura.io/docs/latest/graphql/core/databases/postgres/queries/query-filters.html)
- [Pete Corey - GraphQL NoSQL Injection Through JSON Types](http://www.petecorey.com/blog/2017/06/12/graphql-nosql-injection-through-json-types/)

## 2. A graph database and query engine (codename StarfishQL) for graph analysis and visualization

We want to preform graph analysis and visualization for an inter-related set of entities. For example, we could visualize the dependency network of crates on [crates.io](https://crates.io/)!

There is already some preliminary work done for this project. Checkout the [StarfishQL repository](https://github.com/SeaQL/starfish-ql) and [demo apps](https://starfish-ql.sea-ql.org/). You need to think about it's potential applications and how to make them a reality.

**Deliverables:** Define and enhance the query language, refine and improve the query engine and develop client-side libraries.

**Skills Preferred:**

- Familar with graph analysis
- Experience in Rust & SQL

**Possible Mentors:**

- [Chris Tsang](https://github.com/tyt2y3)
- [Billy Chan](https://github.com/billy1624)
- [Sanford Pun](https://github.com/shpun817)

**Expected Size of Project:** 350 hours

**Difficulty Rating of Project:** Medium

**Reference:**

- https://medium.com/graph-commons/analyzing-the-npm-dependency-network-e2cf318c1d0d

## 3. Support an open source NewSQL database (CockroachDB, TiDB, Presto etc)

This is more career oriented than the other projects, because if you are graduating and finding jobs in the startup world, having experience in NewSQL will definitely make you a star!

Basically we would like to support one of the open source NewSQL databases. CockroachDB is somewhat compatible with Postgres while TiDB is somewhat compatible with MySQL, so if we go for one of these two, we will be developing value-added facilities in the SeaQL ecosystem. If we go after Presto (or a similar non-compatible database), we will have to support it's syntax (SeaQuery), protocol and other lower level aspects of the technology stack. It's entirely up to you, just don't propose a non-open-source database thanks!

**Deliverables:** It could be a query builder and/or a database driver written in Rust for an specific NewSQL database.

**Skills Preferred:**

- Familiar with one of open source NewSQL database, such as CockroachDB, TiDB, Presto, etc.

**Possible Mentors:**

- [Chris Tsang](https://github.com/tyt2y3)
- [Billy Chan](https://github.com/billy1624)
- [Charles Chege](https://github.com/charleschege)

**Expected Size of Project:** 350 hours

**Difficulty Rating of Project:** Medium

## 4. Query linter for SeaORM

SeaORM is dynamic. As such we cannot check for query correctness compile-time. We wanted to support test-time linting, meaning we enable the linter during unit tests / integration tests / CI and disable it during production. The linter should be able to catch syntatic, semantic and logic errors given the schema definition. You can think of it as "Clippy for SeaORM"!

**Deliverables:** A linter for SeaORM to catch errors of SQL queries at test-time.

**Skills Preferred:**

- Familiar with SQL syntax of at least one rational database

**Possible Mentors:**

- [Chris Tsang](https://github.com/tyt2y3)
- [Billy Chan](https://github.com/billy1624)

**Expected Size of Project:** 350 hours

**Difficulty Rating of Project:** Medium

**Reference:**

- https://www.sea-ql.org/SeaORM/docs/write-test/testing
- https://github.com/SeaQL/sea-orm/search?q=lint%3A

## 5. A SQL interpreter primarily intended for Mock testing 

The is by far the most academic oriented project. We already have "rudimentary" Mock testing support in SeaORM. If we are able to implement a basic SQL interpreter, we will be able to move some unit-testing originally requiring SQLite into pure Rust. Note that for the scope of this project, we absolutely do not cater the "harder" aspects of databases, for example, ACID, concurrency, storage etc. It will be a pure in-memory SQL simulator / interpreter with the only concern being correct.

**Deliverables:** A SQL interpreter that can simulate the operation of CRUD SQL statements.

**Skills Preferred:**

- Solid knowledge of how database and SQL works

**Possible Mentors:**

- [Chris Tsang](https://github.com/tyt2y3)
- [Billy Chan](https://github.com/billy1624)

**Expected Size of Project:** 350 hours

**Difficulty Rating of Project:** Hard

**Reference:**

- https://github.com/joaoh82/rust_sqlite
- https://github.com/gluesql/gluesql
