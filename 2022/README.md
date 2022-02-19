# 2022 GSoC Idea List

## 1. A GraphQL framework on top of SeaORM

### Background

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

## 3. Support an open source NewSQL database (CockroachDB, TiDB, Clickhouse etc)

## 4. Query linter for SeaORM

## 5. A SQL interpreter primarily intended for Mock testing 
