# Codebase/Architecture

## 1. How old is your codebase?
Varun started writing Kayako in early 2001, and launched v1 in Nov 2001. The first commit to Kayako was made at 12:02 AM, Feb 13, 2001.

## 2. Do you have an automated test suite?
- **What libraries and tools do you use? What sorts of tests do you use? (unit, integration, system, load, ...)**
- **What is your testing methodology? (BDD, TDD, Spike & Stabilize, ...)**
- **What is your current level of test coverage? Are you happy with it?**

We use Travis CI for continuous integration. For unit testing of PHP codebase, we use PHPUnit. Some of the other tools that we use are PHP Copy Paste Detector, PHPLint, PHP Mess Detector and Code Climate.

There is no one official position on testing methodologies yet and this may vary by project. We have an automated test suite for the API and some automated unit-tests but the code coverage isn't the highest at the time of this writing, we're getting there.

## 3. Do you regularly correct technical debt?

We try our best to not accrue technical debt knowingly but when it does happen, we prioritize fixing it. Over the years, we have learnt the hard way that tech debt can't be wished away and is often more expensive to fix later. Our internal engineering manifesto has strong statements regarding this, here are a few:

Don’t just keep adding arguments to functions, avoid them. Your job is to simplify the existing code, not make it more complex! Every code change, every new parameter to a function, every new class, every new model needs to be questioned. Twice. Thrice. Five times.. forever till you realise and understand that this cannot be improved further.

## 4. On a scale of 1 to 10, how much spaghetti code do you have?

3.43. Don't ask us how we got to that number.

## 5. How well-documented is your codebase?
- **Do you use automated documentation systems like PHPDoc or JSDoc?**
- **Do you maintain a wiki?**

All source code is well-documented (PHPDoc, JSDoc, GoDoc) and we have automated checks to make sure it stays that way. Yes, we do maintain a comprehensive wiki for each project. In fact, engineers are encouraged to fill in the wiki for a project before starting to write actual code.

## 6. Pure CSS, or compiled middleware (LESS, SASS, etc)?

SASS everywhere.

## 7. What browser and operating system versions do you support?

Our targets for full visual and functional support are:

Browsers - IE: 10+, Chrome: 30+, Firefox: 30+, Safari 7+, Opera 23+.

Android - 4.4+, iOS - 8+, Windows Phone - 8+

## 8. Does your codebase require a build process, and is it automated?

Yes and yes.

## 9. Do you have a continuous integration process implemented?

Yes. Code is tested on Travis CI as soon as a PR is opened, and throughout the git-flow stages.

## 10. Do you use MVC or similar code structuring?

We use an in-house MVC framework.

## 11. What is your primary backend language, including version?

*TK* PHP v5.6. We stick to the latest stable version.

## 12. Do you host your product yourself (Local, CoLo, VPS) or is it running on a cloud platform such as AWS or Heroku?

All current Kayako OnDemand servers are running on SoftLayer, our next version will be completely hosted on AWS.

## 13. Do you use open source libraries, and are you aware of the licensing on those libraries?

Yes. Licensing *TK*

## 14. Do you contribute to open source libraries?

Whenever we find ourselves making changes to a third-party library, we consider whether the change could be beneficial for the community and create a PR upstream if so. Here's a recent PR from one of our Go folks - [https://github.com/keimoon/gore/pull/4](https://github.com/keimoon/gore/pull/4)