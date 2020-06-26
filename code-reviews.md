---
title: Code Reviews at OfficeLuv
layout: default
permalink: '/code-reviews'
---

## Why Do Code Reviews?

Doing code reviews:

- shares knowledge of the codebase and business
- catches bugs automated testing may not catch
- uncovers blindspots we may have about the codebase
- improves overall code quality and health
- improves our communication skills

## How OfficeLuv Does Code Reviews

We do code reviews once a day, all together, in person. Doing them this way makes knowledge sharing more efficient. Async reviews also can be requested throughout the day for any work that's blocking or more urgent.

Each dev presents their code by briefly explaining the problem and their overall solution. The dev will walk the group through their code, pointing out anything they like or dislike about it. Other devs then ask questions and may give advice on different approaches. If there's nothing blocking the pull request at the end of this process, the code is merged.

Every dev participates in the code review process the same way, regardless of seniority.

## OfficeLuv Code Review Guidelines
- Prefer asking open-ended questions over opinionated statements
- Make clear which comments are non-blocking or unimportant
- Before offering advice, understand the constraints the developer is working with
- When reviewing feature code, table style discussions for later. Open a separate pull request to change any Rubocop or ESLint configs and review that separately.
- Applaud good work; don't let it be only about criticism
- Code reviews should build trust between all members of the team. Any behavior that diminishes trust should be changed.
