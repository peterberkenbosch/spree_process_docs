# Spree's Release Policy

* Deprecation warnings are to be added in patch releases (i.e. 2.2.1) and the code being deprecated will only be removed in minor versions. For example, if a deprecation warning is added in 2.2.1, 2.2.2 will still contain the same deprecation warning but in 2.3.0 the deprecation warning and the code will be gone.

* Master branch receives *all* patches, including new features and breaking API changes (with deprecation warnings, if necessary).

* One branch "back" from master (currently 2-4-stable) receives patches that fix all bugs, and security issues, and modifications for recently added features (for example, split shipments). Breaking API changes should be avoided, but if unavoidable then a deprecation warning MUST be provided before that change takes place.

* Two branches "back" from master (currently 2-3-stable) receives patches for major and minor issues, and security problems. Absolutely no new features, tweaking or API changes.

* Three branches back from master (currently 2-2-stable) receives patches for major issues and security problems. The severity of an issue will be determined by the person investigating the issue. Absolutely no features, tweaking or API changes.

* Four branches and more "back" from master (currently 2-1-stable and lesser) receive patches only for security issues, as people are still using these branches and may not be able to or wish to upgrade to the latest version of Spree.

To determine how often minor branches of Spree are released, please check the [RubyGems version page for Spree](http://rubygems.org/gems/spree/versions).

We strongly encourage people to upgrade to using the latest Spree releases to avoid being stuck on a release that is no longer maintained.
