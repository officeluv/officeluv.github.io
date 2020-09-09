---
title: OfficeLuv's Retrospective Takeaways
layout: default
permalink: '/takeaways'
---

Every week during our [retrospectives](/retrospectives), we like to document our major takeaways from the iteration. Some of our takeaways are specific to our products, others relate to the tools, languages, and processes that we use, and some relate to programming in general.

We enjoy looking back through all the takeaways we've collected over the years, and thought some of them could be useful to others, especially to those interested in Ruby on Rails or React.js.

### September 9, 2020
- SQL code, just like procedural code, can usually be refactored/reordered for speed improvements.
- People will eventually always forget about the default value in a form and have issues when they submit the default value accidentally.

### August 26, 2020
- More flexibility in configuration = more rules to follow.

### August 19, 2020
- Smaller design/UX issues can easily open up larger ones.
- When planning out new features, keep in mind how you would explain how the feature works to the rest of the company.

### August 12, 2020
- The smallest changes can have big impacts on our internal users (e.g. sending Slack messages to a common channel).
- Our demo/sales environment is always much more different from production than we think.
- Don't rely on dependencies of your dependencies (or things will break when the stated dependency is removed).

### August 5, 2020
- Make sure the docs you’re reading pertain to the library version you want to use.
- Improving search results relevance requires a lot of refinements and experimentation over time.

### July 29, 2020
- _Always_ check that the feature you’re trying to implement is supported by your current plan/level in your vendor.

### July 22, 2020
- Your userbase probably has multiple types of users, one of which is likely your own internal employees.
- Features built for individual users have a good chance of being replicated for user groups and vice versa.

### July 15, 2020
- [React] Having consistent API responses and redux schemas makes reusing React components a lot easier.
- CI outages/bugs are good reminders of how much we rely on a stable CI pipeline for peace of mind.

### July 8, 2020
- Event sourcing introspection is becoming increasingly important for queries we write, because we often need to know the state of a given record at a certain moment in time.

### July 1, 2020
- It’s worth considering what UX principles we’re unwilling to negotiate on when getting an MVP out the door.
- Reusing the same authorization logic universally throughout the system comes at a performance cost.

### June 17, 2020
- When writing automated tests for controllers, you often end up testing much lower level things rather than the controller itself.
  - You should have the base of the testing pyramid before testing the specs, or bugs unrelated to the controller specs will surface.
- Remove sensitive data from serialized data at the lowest level possible, before external serialization logic.

### June 10, 2020
- It’s best for model concerns not to introspect the record using that concern, but rather have methods that the models implement that conform and normalize data needed for the concern to work.
- Sometimes it’s necessary to just “take a stroll” through the data and the code to identify unusual behavior, and to dig into why that might be happening.

### June 4, 2020
- [React] Take the time to avoid deriving state from props. It will play nicer with React and other components down the road.
- Learn about the Serializer/Deserializer (SerDes) methods and techniques in your particular language/framework - they have compounding effects!

### May 26, 2020
- Glad we’re on Rails 6 because now we can take advantage of its database functionality.
  - Another reason to do your upgrades early, because if we had waited, we’d have even more things to migrate over.
  - You’re constantly investing in your current structure, so if you know you need to upgrade regardless, invest in that instead.

### May 13, 2020
- [Rails] It’s okay to use FactoryBot in seeds. If you rely on FactoryBot for testing, It’ll make setup easier and more consistent with your test data. A major drawback is that there’s no good f`ind_or_create_by` method with factories, which is often used to make seeding idempotent.
- Moving a record's preferences from a separate model onto the record itself reduced extra db queries, and allowed for better data integrity guarantees. It also greatly simplified the editing of them on our platforms.

### May 6, 2020
- [React] The bootstrapping/loading of our single-page app has become very complex.
- [React] `ComponentDidUpdate` lifecycle methods may be unavoidable in some cases, but should be considered a code smell.
- Maybe it’s worth experimenting with breaking out business logic flows into separate classes, out of the models and jobs we currently use for it.

### April 29,2020
- Issue-free projects have no guarantee of continuing to be issue-free.

### April 15, 2020
- When expanding an existing tool, try to extract a base that other classes can inherit from. This makes it more extensible and testable.
- Patterns should be enforced within code and classes.
- Remember how adding components to UI affects how that page looks when printed.


### April 8, 2020
- [Ruby] Whenever possible, create and/or use classes instead of passing hashes into Ruby library code. Classes provide data validation and encapsulation.
- Documentation that gives a flow or step-by-step process tends to be more helpful than widely-dispersed and extensive docs.

### April 1, 2020
- Our Authorization logic is becoming a central and more consequential element of our app, so we need to decompose it and write tests around it.
- Changing your Audience/Users requires changes to every part of the business, and has ripple effects everywhere.
- Releasing more frequently takes more time away from building/fixing other things, so there’s a balance to deployment frequency and building features.
- We could leverage partial database indices more in our app.
- State management complexity increases exponentially as more states are added.




