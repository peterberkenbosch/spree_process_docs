# Spree's Release Management

We strongly encourage people to upgrade to using the latest Spree releases to avoid being stuck on a release that is no longer maintained.

## Policy

* Master branch receives *all* patches, including new features and breaking API changes (with deprecation warnings, if necessary).

* One branch "back" from master (currently 2-4-stable) receives patches that fix all bugs, and security issues, and modifications for recently added features (for example, split shipments).

* We support the last 4 stable branches back from master, ie. 2-4-stable, 2-3-stable, 2-2-stable and 2-1-stable at the time of this writing. Support means that we includes those branches in the release cycle (see below).
__todo__ timeboxed support for older versions?

* Deprecation warnings are to be added in patch releases (i.e. 2.2.1) and the code being deprecated will only be removed in minor versions. For example, if a deprecation warning is added in 2.2.1, 2.2.2 will still contain the same deprecation warning but in 2.3.0 the deprecation warning and the code will be gone.

You can find all the release on the [RubyGems version page for Spree](http://rubygems.org/gems/spree/versions) and on [Spree Github Releases page](https://github.com/spree/spree/releases)

## Release cycle

* Regular patch releases are done for the supported branches every 2 weeks, so for 2.4.0 we will release 2.4.1 in 14 days, these patches will contain only bug and security fixes. No new features and no breaking API changes.

* Regular (non breaking API) feature releases are a minor release. So with the 2.4.0 example, we will release a 2.5.0 version.

* Larger and breaking API feature releases will are a major release. Again with the 2.4.0 example, we will release a 3.0.0 verion.

### Ad-hoc releases

With security issues, it could be needed to release a patch version outside of the cycle. When needed we will release security patches ad-hoc with a new patch release.

## What's included in every release

Every release will have the following:

* a changelog describing what has changed,
* an upgrade guide with detailed step by step documentation on how to upgrade,
* a tag in the github repository with the corresponding version,
* a release in the github repository linking the changelog and the upgrade path,
* an entry in the rubygems
