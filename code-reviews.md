---
title: Code Reviews at OfficeLuv
layout: default
permalink: '/code-reviews'
---

## Why Do Code Reviews?

Doing code reviews:

- shares knowledge of the codebase and business
- catches bugs automated testing may not catch
- uncovers optimizations and opportunities for collaboration that may otherwise stay siloed
- uncovers blindspots we may have about the codebase
- improves overall code quality and health
- improves our communication skills

## How OfficeLuv Does Code Reviews

We do code reviews once a day, all together, in person or over video chat. Doing them this way makes knowledge sharing more efficient. Async reviews also can be requested throughout the day for any work that's blocking or more urgent.

Each dev presents their code by briefly explaining the problem and their overall solution. The dev will walk the group through their code, pointing out anything they like or dislike about it. Other devs then ask questions and may give advice on different approaches. If there's nothing blocking the pull request at the end of this process, the code is merged.

Every dev participates in the code review process the same way, regardless of seniority.
Code Review is also a time reserved for reviewing external code. This can be open-source work members are currently working on, something they were proud of cracking, or just an interesting link or library.
We also review applicant code samples as a group during our Code Review sessions - just as we would review our own code.

## OfficeLuv Code Review Guidelines
- Adhere to our [code of conduct](/code-of-conduct)
- Prefer asking open-ended questions over making opinionated statements
- Make clear which comments are non-blocking or unimportant (ideally adhering to [conventional comments syntax](https://conventionalcomments.org)) 
- Use inline-change suggestions where possible to minimize minor editing workload on the originator
- Before offering advice, understand the constraints the developer is working with
- When reviewing feature code, table style discussions for later. Open a separate pull request to change any Rubocop or ESLint configs and review that separately.
- Applaud good work; don't let it be only about criticism
- Code reviews should build trust between all members of the team. Any behavior that diminishes trust should be changed.

## Further Reading

- [The benefits of daily code review](https://www.joshbeckman.org/2016/08/11/the-benefits-of-daily-code-review/)
- [Conventional comments](https://conventionalcomments.org)
