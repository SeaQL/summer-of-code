# GSoC 2023 Ideas List

Welcome! If you haven't read the [GSoC Contributing Guide](CONTRIBUTING.md) please read it first before going through the ideas list.

Prospective contributors, please open a discussion with us on [Discussions](https://github.com/SeaQL/summer-of-code/discussions)!

## 1. Expand the features of [SeaORM](https://github.com/SeaQL/sea-orm) - An async & dynamic ORM for Rust

SeaORM is the flagship project of SeaQL. We are now approaching our first stable release. We have set a solid [architecture](https://www.sea-ql.org/SeaORM/docs/internal-design/architecture/) for expanding the usefulness of an ORM in building data-driven applications, but there is still more to be desired. During this Summer of Code project, you will be involved in one full release cycle and go through it from design to delivery. SeaORM is a maturing project, so the experience will be different from a greenfield "from scratch" project. But we assure the process will be as much fun and much more impactful. Here is an outline of the process:

1. Idea. Draft and refine several ["Proposal & Implementation Plan" (PIP)](https://github.com/SeaQL/sea-orm/issues?q=is%3Aissue+%5BPIP%5D)s
2. Implementation. Implement the feature following our [Engineering Practices](https://www.sea-ql.org/blog/2022-07-30-engineering/)
3. Review. Solicit reviews and improve upon the implementation following our [Review Guidelines](https://www.sea-ql.org/blog/2023-01-01-call-for-contributors-n-reviewers/#what-are-the-criteria-when-reviewing-a-pr)
4. Documentation. Write throughout documentation and may be tutorials to guide users of the new feature
5. Release. Co-author the release notes and make an announcement

Tips for drafting a proposal: it is important to have had first-hand experience using SeaORM. Identify one or more aspects you want to improve, and focus on them. Here are several suggestions, but feel free to come up with yours. Include no more than 3 major features in your proposal.

1. Migration template and generation https://github.com/SeaQL/sea-orm/discussions/645
1. Customisation aware entity generation https://github.com/SeaQL/sea-orm/issues/1931
1. Entity first workflow (e.g. https://learn.microsoft.com/en-us/ef/ef6/modeling/code-first/migrations/automatic I am sure there is a discussion thread somewhere)
1. Deeply nested select https://github.com/SeaQL/sea-orm/discussions/1502

**Deliverables:** 1, 2 or at most 3 major features in a SeaORM release

**Skills Required:**

- Hands on experience with SeaORM
- Solid knowledge in Rust and SQL

**Possible Mentors:**

- [Chris Tsang](https://github.com/tyt2y3)
- [Billy Chan](https://github.com/billy1624)

**Expected Size of Project:** 350 hours

**Difficulty Rating of Project:** Medium

## 2. Expand the features of [FireDBG](https://github.com/SeaQL/FireDBG.for.Rust/) - Time Travel Visual Debugger for Rust

FireDBG is our new undertaking, probably a too-ambitious one. It is still in the early days, a lot is yet to be done/defined, so there is maximum room for creativity. FireDBG is dependent on Rust's ABI, which means we are forced to release whenever a new rustc comes out every 6 weeks.

A few ideas:

1. Test and fix bugs for capturing complex values
1. Implement a set of interesting algorithms in Rust and improve FireDBG's visualizations
1. Support inspection of all standard library types (Mutex, Channel, etc)
1. Design a plugin system to support third party crates
1. Perform more advanced static analysis (based on Rust Analyzer)

**Deliverables:** 1, 2 or at most 3 major features in a FireDBG release

**Skills Required:**

- Hands on experience with FireDBG
- Solid knowledge in Rust the language and the compiler

**Possible Mentors:**

- [Chris Tsang](https://github.com/tyt2y3)
- [Billy Chan](https://github.com/billy1624)

**Expected Size of Project:** 350 hours

**Difficulty Rating of Project:** Hard