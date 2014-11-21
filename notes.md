# Process Spree

* Hotspot Area's
** Order Update
** Checkout flow
** Callbacks AR / Statemachine
** Destructive code

* 'Mantras' / Rules
* Moderation flow
* Ruby guide lines
* Spree guide lines
* Code metrics -> CodeClimate
* Performance benchmarking -> "golden path"
* Voting / Review trigger.. ie when do we need more input / reviews.

* README -> Development vs User
* Spree Wiki

# Expertise groups
* core experts list
* component tag / gh

# PR
* Tagging component for review by core experts

# Measurement tools
* HoundCI
* Brakeman
* Bullet
* JMeter -> flood.io / blitz


# Platform
* Slack
* Spree Wiki
* IRC
* User Group


# Ideas about handling stable branches
* Applying semver as best as we can
* Time boxed bug fixes on stable branches
* Only security fixes
* Smaller releases
* Faster releases

What to backport and how to backport

# Tagging issues and PRs guidelines.
* list tags and rational for use

# Blog posts
* to_prepare block for settings. Bonobos.. (needs more info)


----
# Spree::Process

* What’s our funnel
* Ruby/Spree styleguide
* PR guidelines
* Getting involved page
* Clean up README (spree/spree)
* Benchmarks for performance
* Turn on code climate for pull requests
* HoundCI
* Count sql queries
* Issue/PR tagging based on subject
* What about test guidelines
* Expect a PR to include a failing and passing spec
* Issues / Feature requests
* User voice?

How we’ve improved the process (the blog post)
* Better tools
* Rules
* …..
* Updated Readme
* Get in touch with us!
* We’re moving to YARD
*

## Rules

* Don’t decorate state machine (see roadmap)
* No callbacks
* Public API changes will need justification
* Limit (avoid) adding actions to controllers & models
* Performance can’t take a hit
* No additional queries
* Encourage removing code!
* If it breaks other tests
* Non-localized strings will be rejected
* Destruction or change data
* Avoid adding new gem dependency
* API endpoints need to proper authentication/authorization
* Don’t mention people in commits


## Components

* Admin
* Promo
* Returns
* API
* Stock/Inventory
* Adjustments
* Order Management
* Checkout
