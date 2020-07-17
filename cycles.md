---
title: Development Cycles at OfficeLuv
layout: default
permalink: '/cycles'
---

We operate and deliver solutions in weekly cycles (or iterations).
The week size allows us enough time to work on something substantial enough for the customer to use, while also constraining us to pare down a feature set to essential components.
Each cycle usually consists of new feature work, feature iteration and extension, and bug fixes.

## Cycle Stages

Based on the usage patterns within our product, Tuesday is lowest throughput day of the week, so we generally deploy any new features on Tuesday afternoon.
We exclusively use CI/CD pipelines to deploy, and hotfixes or minor features are deployed throughout the week if necessary.

Generally, we begin each cycle on Wednesday morning with a [retrospective session](/retrospectives) to review the previous cycle and document feedback and takeaways.
On Wednesday we also plan out the new cycle as a group, selecting, grouping, and scoring stories in a loose [Kanban style](https://en.m.wikipedia.org/wiki/Kanban).
Most stories are not assigned to a particular member, instead we generally allow any story to be picked up by a member that is free and interested.
After planning, team members begin development, design, or research work on stories.

Each day in the week, we will conduct [code review sessions](/code-review) for code, design, documentation, or research results before they are made available in our staging environment.
Once a story has moved to a stage where it is ready for QA or testing, another team member will spend time testing the bugfix or feature or will work through acceptance with stakeholders.
If a solution fails this testing stage, it is documented and moved into a failed state, where it can be picked up by the originally-implementing team member to be worked on again.
Solutions and stories that pass the testing stage are marked as ready for deployment.

The following Tuesday afternoon, we spend time updating [changelogs](#changelogs) and marking [versions](#versioning) in our repositories, which triggers our deployment pipelines.
Immediately following this deployment, we send out a [product release email](https://www.joshbeckman.org/2020/05/24/writing-great-product-release-emails/) describing the cycle's changes and the next cycle's themes.
This marks the end of a cycle, and we begin the process again on Wednesday morning.

## Roles

We practice switching roles between team members for processes in our cycle.
This means that we take turns:
- updating changelogs and tagging new versions (deploying)
- writing the product release email
- documenting our [retrospective](/retrospectives)
- leading the cycle story planning session

## Changelogs

For our open source libraries and most of our internal repositories, we maintain a `CHANGELOG.md` at the root of the project.
We follow the [keep a changelog](https://keepachangelog.com/en/1.0.0/) format and create a new entry for any version change.

## Versioning

We follow [semantic versioning](https://semver.org/spec/v2.0.0.html) for all of our repositories/codebases.
This generally means that each cycle ends with a new minor version for a given codebase.
A hotfix/bugfix change will yield a patch version change.
We generally reserve major version changes for major redesigns of the customer interface (new branding, etc).

## Deploys Vs. Releases

We generally observe a difference between a feature being _deployed_ and its _release_.

We consider a feature deployed if the code for the feature is live and available in a production environment.
A feature is released if it has been deployed _and_ it is available for use by customers in the general experience flow and is documented/sold to customers.
