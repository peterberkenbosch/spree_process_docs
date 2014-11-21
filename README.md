# Process Docs

Placeholder repo to keep the docs and notes versioned.

## Todo

* TOC
* Developer docs for using Spree vs Developer docs for contribution to Spree
* Break things out in smaller bits
* Build developer site around it


## Ruby Styleguide

We started by applying the [Thoughtbot Styleguide](https://github.com/thoughtbot/guides/blob/master/style/README.md)
this will be enforced for every pull request. We use [HoundCI](https://houndci.com) for that, so when
you violate a style rule there will be a comment on that specific line in your pull request.

## CodeClimate code quality

We also run [CodeClimate](https://codeclimate.com/github/spree/spree) on all pull requests, low quality code needs to be refactored before we consider accepting the pull request.

## Ruby documentation with YARD

Comment the public api interface with YARD, for usage see the [YARD Getting Started](http://www.rubydoc.info/gems/yard/file/docs/GettingStarted.md) page.
