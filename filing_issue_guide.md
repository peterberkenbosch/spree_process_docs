## Filing an issue

When filing an issue on the Spree project, please provide these details:

* A comprehensive list of steps to reproduce the issue.
* What you're *expecting* to happen compared with what's *actually* happening.
* The version of Spree *and* the version of Rails.
* Your application's complete `Gemfile.lock`, and `Gemfile.lock` as text in a [Gist](https://gist.github.com) (*not as an image*)
* Any relevant stack traces ("Full trace" preferred)

In 99% of cases, this information is enough to determine the cause and solution
to the problem that is being described.

Please remember to format code using triple backticks () so that it is neatly
formatted when the issue is posted.

Any issue that is open for 14 days without actionable information or activity
will be marked as "stalled" and then closed. Stalled issues can be re-opened if
the information requested is provided.

_Please do not assign labels or create new labels to your issue. We will assign the appropriate labels to ensure your ticket is handled in the appropriate manner._


#### When to File an Issue

You should file an issue if you have found (or suspect) a bug in the "core" functionality of Spree. If you have found a bug in one of the extensions, please file an issue with the appropriate extension project in GitHub. If you're not sure if the behavior you're experiencing is intentional just ask on the mailing list and someone will encourage you to file a ticket if your issue sounds like a bug (as opposed to a feature.)

#### How We Prioritize Issues

Spree is a very large project with lots of activity. We try our best to respond to all of the questions and issues our users have.  We use the following criteria to prioritize issues:

* Does this bug effect the latest stable release?
* Are there details on how to reproduce the problem?
* Is there a patch associated with the issue?
* Is there a test included in the patch?
* Has someone else verified the bug?

We give highest priority to issues where the answer is "yes" to all of these questions. Next highest priority is for issues that answer "yes" to most of these questions, particularly the first few criteria.


_You need to include a brief description of the problem and simple steps needed to reproduce it. If you fail to supply this minimum level of information your issue will likely be ignored._
