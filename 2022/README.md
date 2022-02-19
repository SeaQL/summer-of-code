# 2022 GSoC Idea List

## 1. A GraphQL framework on top of SeaORM

We would like to have a GraphQL framework / engine that build's on top of SeaORM. It is now doable to roll your own GraphQL solution using SeaORM, but it is so cumbersome and every resolver has to be coded by hand. We could take inspiration from [awto](https://github.com/awto-rs/awto), where database schema follows a set convention, so that we are able to provide common GraphQL operations (pagination, filtering, sorting, joining etc) out-of-the-box. We can also take inspiration from Hasura or Dgraph of developing a GraphQL engine. The exact approach has to be discussed, as we do not want to duplicate Hasura, which is itself a pretty great open source project.

### Reference

<p><span style="font-size:12pt"><span style="font-family:&quot;Times New Roman&quot;,serif"><span style="font-size:11.0pt"><span style="font-family:&quot;Calibri&quot;,sans-serif"><a data-darkreader-inline-color="" href="https://www.prisma.io/blog/how-to-wrap-a-rest-api-with-graphql-8bf3fb17547d" style="color: blue; text-decoration: underline; --darkreader-inline-color:#337dff;">Wrap a REST API with GraphQL - A 3-step tutorial | Prisma</a></span></span></span></span></p>

<p><span style="font-size:12pt"><span style="font-family:&quot;Times New Roman&quot;,serif"><span style="font-size:11.0pt"><span style="font-family:&quot;Calibri&quot;,sans-serif"><a data-darkreader-inline-color="" href="https://www.apollographql.com/blog/graphql/filtering/how-to-search-and-filter-results-with-graphql/" style="color: blue; text-decoration: underline; --darkreader-inline-color:#337dff;">GraphQL Search and Filter &ndash; How to search and filter results with GraphQL - Apollo GraphQL Blog</a></span></span></span></span></p>

<p><span style="font-size:12pt"><span style="font-family:&quot;Times New Roman&quot;,serif"><span style="font-size:11.0pt"><span style="font-family:&quot;Calibri&quot;,sans-serif"><a data-darkreader-inline-color="" href="https://docs.fauna.com/fauna/current/api/graphql/relationships" style="color: blue; text-decoration: underline; --darkreader-inline-color:#337dff;">GraphQL relationships | Fauna Documentation</a></span></span></span></span></p>

<p><span style="font-size:12pt"><span style="font-family:&quot;Times New Roman&quot;,serif"><span style="font-size:11.0pt"><span style="font-family:&quot;Calibri&quot;,sans-serif"><a data-darkreader-inline-color="" href="https://graphql.org/learn/queries/" style="color: blue; text-decoration: underline; --darkreader-inline-color:#337dff;">Queries and Mutations | GraphQL</a></span></span></span></span></p>

<p><span style="font-size:12pt"><span style="font-family:&quot;Times New Roman&quot;,serif"><span style="font-size:11.0pt"><span style="font-family:&quot;Calibri&quot;,sans-serif"><a data-darkreader-inline-color="" href="https://dgraph.io/docs/graphql/queries/search-filtering/#filter-a-query-for-a-range-of-objects-with-between" style="color: blue; text-decoration: underline; --darkreader-inline-color:#337dff;">Search and Filtering - GraphQL (dgraph.io)</a></span></span></span></span></p>

<p><span style="font-size:12pt"><span style="font-family:&quot;Times New Roman&quot;,serif"><span style="font-size:11.0pt"><span style="font-family:&quot;Calibri&quot;,sans-serif"><a data-darkreader-inline-color="" href="https://romankudryashov.com/blog/2020/12/graphql-rust/" style="color: blue; text-decoration: underline; --darkreader-inline-color:#337dff;">GraphQL in Rust | Roman Kudryashov&#39;s tech blog</a></span></span></span></span></p>

<p><span style="font-size:12pt"><span style="font-family:&quot;Times New Roman&quot;,serif"><span style="font-size:11.0pt"><span style="font-family:&quot;Calibri&quot;,sans-serif"><a data-darkreader-inline-color="" href="https://hasura.io/blog/building-a-graphql-to-sql-compiler-on-postgres-ms-sql-and-mysql/" style="color: blue; text-decoration: underline; --darkreader-inline-color:#337dff;">Building a GraphQL to SQL Compiler on Postgres, MS SQL, and MySQL (hasura.io)</a></span></span></span></span></p>

<p><span style="font-size:12pt"><span style="font-family:&quot;Times New Roman&quot;,serif"><span style="font-size:11.0pt"><span style="font-family:&quot;Calibri&quot;,sans-serif"><a data-darkreader-inline-color="" href="https://hasura.io/docs/latest/graphql/core/databases/postgres/queries/query-filters.html" style="color: blue; text-decoration: underline; --darkreader-inline-color:#337dff;">Postgres: Filter query results / search queries | Hasura GraphQL Docs</a></span></span></span></span></p>

<p><span style="font-size:12pt"><span style="font-family:&quot;Times New Roman&quot;,serif"><span style="font-size:11.0pt"><span style="font-family:&quot;Calibri&quot;,sans-serif"><a data-darkreader-inline-color="" href="http://www.petecorey.com/blog/2017/06/12/graphql-nosql-injection-through-json-types/" style="color: blue; text-decoration: underline; --darkreader-inline-color:#337dff;">Pete Corey - GraphQL NoSQL Injection Through JSON Types</a></span></span></span></span></p>

## 2. A graph database and query engine (codename StarfishQL) for graph analysis and visualization

We want to preform graph analysis and visualization for an inter-related set of entities. For example, we could visualize the dependency network of crates on crates.io!

There is already some preliminary research done internally for this project and so it is not entirely from scratch.

### Reference

https://medium.com/graph-commons/analyzing-the-npm-dependency-network-e2cf318c1d0d

## 3. Support an open source NewSQL database (CockroachDB, TiDB, ClickHouse etc)

This is more career oriented than the other projects, because if you are graduating and finding jobs in the startup world, having experience in NewSQL will definitely make you a star!

Basically we would like to support one of the open source NewSQL databases. CockroachDB is somewhat compatible with Postgres while TiDB is somewhat compatible with MySQL, so if we go for one of these two, we will be developing value-added facilities in the SeaQL ecosystem. If we go after ClickHouse (or a similar non-compatible database), we will have to support it's syntax (SeaQuery), protocol and other lower level aspects of the technology stack. It's entirely up to you, just don't propose a non-open-source database thanks!

## 4. Query linter for SeaORM

SeaORM is dynamic. As such we cannot check for query correctness compile-time. We wanted to support test-time linting, meaning we enable the linter during unit tests / integration tests / CI and disable it during production. The linter should be able to catch syntatic, semantic and logic errors given the schema definition. You can think of it as "Clippy for SeaORM"!

### Reference

https://www.sea-ql.org/SeaORM/docs/write-test/testing
https://github.com/SeaQL/sea-orm/search?q=lint%3A

## 5. A SQL interpreter primarily intended for Mock testing 

The is by far the most academic oriented project. We already have "rudimentary" Mock testing support in SeaORM. If we are able to implement a basic SQL interpreter, we will be able to move some unit-testing originally requiring SQLite into pure Rust. Note that for the scope of this project, we absolutely do not cater the "harder" aspects of databases, for example, ACID, concurrency, storage etc. It will be a pure in-memory SQL simulator / interpreter with the only concern being correct.

### Reference

https://github.com/joaoh82/rust_sqlite
https://github.com/gluesql/gluesql
