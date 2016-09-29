# Development Process

## 1. What will be my day to day responsibilities? How much time do you anticipate I would spend on each one?

This depends on your role and designation. There are no hard limits on the time you’re expected to spend - most of our engineers spend an average of 8-9 hours in office per day. This is totally upto you though, it doesn’t matter as long as you get the stuff done.

## 2. What source control do you use? Can you explain why you chose it?

We use Git. It’s distributed, and makes it easy to rewrite/patch up history.

## 3. Are your repos hosted in-house or on a third-party service? GitHub?

All our code (except some salesforce code, which is directly hosted on their servers) is hosted on GitHub.

## 4. What is your workflow currently, with regards to developers pushing changes. Do you do pull requests, or does everyone just merge to a central repo?

Pull requests. Merging your own PRs is a cardinal sin.

## 5. Are you using a ticket system or is it more play it by ear? Do you use the same system for both bugs and new features?

We use JIRA for both bugs and features. Every task being worked on at Kayako has a ticket behind it.

## 6. Do you have a code review process?

Yes, we do. Every PR is reviewed by at least one other person before it's merged.

## 7. Does your team encourage the use of SOLID and DRY design principles to avoid cyclomatic complexity?

Yes, absolutely! Here’s a snippet from our internal Engineering Manifesto:

Every code change, every new parameter to a function, every new class, every new model needs to be questioned. Twice. Thrice. Five times. Forever till you realise and understand that this cannot be improved further.

Most of the technical debt happens when you don’t think and just layer code or hope for a quick fix. DONT DO THAT. THINK. EVERY SECOND. EVERY MINUTE. QUESTION YOURSELF.

## 8. What is your take on object calisthenics?

We think that they’re overkill. They’re good as ‘suggestions’ to try out in your code - but not as strict rules to follow.

## 9. What is your team's process for choosing, adding, and removing third-party code libraries?

We look for projects that are:

- Actively maintained
- Production-ready (have other big companies using them)
([https://github.com/ziadoz/awesome-php](https://github.com/ziadoz/awesome-php) is a great resource)

If such a project is not available, we evaluate other solutions thoroughly as a team before making a decision.

## 10. Do you have established code style rules? - Did you create your own style guide, or are you using a third party's (PEP8, PSRs, Standard JS, etc) - Is there an automated linting process to validate your styles? - Tabs or spaces? (If relevent) - Allman or BSD braces? (If relevent) - Semicolons? (If relevent)

We have our own in-house style guide for PHP. For repos in Golang, we use gofmt to format code. For JS, JavaScript standard style.
Wherever possible, we do use automated checks (PHP CodeSniffer, GoLint) to enforce these standards.

## 11. What are your development environments like? - Virtual Machines? Local (VirtualBox) or Remote (ESXi)? - Does everyone have an identical development environment? - Are you using vagrant and/or puppet/chef? - How closely do the dev environments mirror your production environment?

We use Vagrant + Chef to manage our dev environments. Everyone works on a standard vagrant box that is actively maintained to mimic our production environment. There are certain differences that are inevitable though, for example - We run on Amazon, Linux at AWS, for example - and our Vagrant boxes run CentOS 6.5.

## 12. What is your release schedule like?

We release three times a week, with ample time for QA testing and feedback in between.

## 13. Do you maintain separate release and dev branches? (git-flow?)

Yes, we do. We use standard git-flow for all repos.

## 14. Will I be provided with a new laptop? - Windows, Mac or Linux? Do I get a choice? - Am I allowed to install anything I want on that laptop? - Will it have an SSD and as much ram as can fit? - How hard do I have to justify software purchases? - How often will I receive hardware upgrades?

Yes! You’ll get a fresh top-line Macbook Pro and Thunderbolt display to work with. What you install on it is upto you, wipe out the whole OS and install ubuntu if you’d like! There’s no hard process on software purchases, but if it helps you do your job and is priced reasonably it’s very unlikely that a request will be denied.

## 15. Which comes first, bugs or features? Are detailed requirements for both determined and documented prior to work beginning?

Bugs come first. Yes, requirements are documented prior to beginning work. We focus on clear documentation, engineers often spend 80% of their time clearly documenting what they’re about to do (and why) - and 20% writing code.
 
## 16. Single product, or will I be regularly working on different projects?

One can expect to work on 2 to 3 different projects every year if not more - the number depends on the size of the project and other business realities but it should be in the ballpark.

## 17. Will I communicate directly with clients on a regular basis, or does this typically happen through an intermediary?

Unless you're working on a public integration/client library, all interactions with clients will be through our sales & support team.