# Release policy

We will follow [SemVer](http://semver.org/) the best we can, we will release a
new major release when we break the public interface.

## Small releases

We thrive to make the releases as small as posible so upgrading to specific
releases are small and have clear steps. Every release will have a well documented
upgrade path to follow.

## Supported branches

We support the last 2 stable branches down the current stable. This means we will actively add
bug- and security fixes. We will *not* add new features to the stable branches. The stable branches
are meant to be and stay stable at all cost.

New features are more then welcome, but that will result in new (minor or major) releases.

## What to do when my changes are not merged?

Since we do not merge new features in the stable branches we suggest that you either
fork the spree repository and merge your changes there, or that you create an extension
that contains the changes you need for the specific branch.

_todo_ link to documentation on how to make that happen.
