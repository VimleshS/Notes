# Relay

Relay is a GraphQL client library for React.

* [Turbine](https://medium.com/chute-engineering/turbine-a1f55d4b7d91)
* [react-transmit: Relay-inspired based on Promises instead of GraphQL](https://github.com/RickWong/react-transmit)
* [**Relay for visual learners**](http://sgwilym.github.io/relay-visual-learners/)
* [The Problem with Data Fetching in React](http://www.sitepoint.com/react-data-fetching-with-relay/)
* [Relay-inspired based on Promises instead of GraphQL](https://github.com/RickWong/react-transmit)

## GraphQL

* [Learn GraphQL](https://learngraphql.com/)
* [Apollo Blog](https://dev-blog.apollodata.com/)
* [GraphQL: The next generation of API design](https://dev-blog.apollodata.com/graphql-the-next-generation-of-api-design-f24b1689756a#.yu0wy14q3)
* [GraphQL on Rails](https://medium.com/@khor/relay-facebook-on-rails-8b4af2057152#.l4mw5w6uz)
* [**Awesome Graphql**](https://github.com/chentsulin/awesome-graphql)
* [GraphQL in the age of REST APIs](https://medium.com/chute-engineering/graphql-in-the-age-of-rest-apis-b10f2bf09bba)
* [Reference implementation in JavaScript](https://github.com/graphql/graphql-js)
* [Issue #26: Reducing executor](https://github.com/graphql/graphql-js/issues/26)
* [**Creating a GraphQL Server**](https://www.youtube.com/watch?v=gY48GW87Feo)
* [GraphQL overview](https://blog.risingstack.com/graphql-overview-getting-started-with-graphql-and-nodejs/)
* [Your first GraphQL Server?](https://medium.com/@clayallsopp/your-first-graphql-server-3c766ab4f0a2)
* [GraphQL and REST](http://blog.startifact.com/posts/graphql-and-rest.html)

---

* Langauge agnostic
* Solve over-fetching and under-fetching
* Not a language, it's an API.
* Client specifies what fields and relationships it wants to get back, not determined by the server!
* Always send 1 request and get back the smallest possible response it needs
* Exposes a single endpoint
* Endpoint parses and executes a query
* Executes over a type system
* Type system available via introspection

```
{
  employments(S6414) {
    service_code,
    project_id,
    timesheets {
      timesheet_id,
      work_month    }  }}
```

Does that mean REST is dead. Not really because lots of companies invested heavily on REST APIs.

GraphQL queries go to GraphQL server where it can source from database queries or other REST servers. It can essentially acts as an intelligent proxy.

---
See Om Next approach on changing a state tree to a graph one, sort of like GraphQL and Falcor.

> The tree is really a graph

A single state tree (i.e. Baobab) can be easily navigated by a cursor. However, visited different branch of a tree prove tedious.

With graph, you can sort of visit anywhere you like! Query let you navigate the graph of your data in all sorts of directions.

Your data is a graph, but what your UI sees is a tree.

### GraphQL Core

* Frontend (Lexer/Parser)
* Type System
* Introspection
* Validation
* Execution - Walking the AST. Parallelism with resolve (Promises).

