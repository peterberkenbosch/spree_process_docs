# Pull Requests

We gladly accept [pull requests](https://help.github.com/articles/using-pull-requests) that add documentation, fix bugs and, in some circumstances,
add new features to Spree.

Here's a quick guide:

1. [Fork the repo.](https://help.github.com/articles/fork-a-repo/)

2. Run the tests. We only take pull requests with passing tests, and it's great
to know that you have a clean slate:

```shell
$ bundle
$ bundle exec rake
```

3. Create a new [topic branch](#topic_branches) then make changes and add tests for your changes. Only
refactoring and documentation changes require no new tests. If you are adding
functionality or fixing a bug, we need tests!

4. Push to your fork and submit a pull request. If the changes will apply cleanly
to the latest stable branches and master branch, you will only need to submit one
pull request.

5. If a PR does not apply cleanly to one of its targeted branches, then a separate
PR should be created that does. For instance, if a PR applied to master & 2-1-stable but not 2-0-stable, then there should be one PR for master & 2-1-stable and another, separate PR for 2-0-stable.

At this point you're waiting on us. We like to at least comment on, if not
accept, pull requests within three business days (and, typically, one business day).
We may suggest some changes or improvements or alternatives.

Make sure you address all the (automatic) feedback on your commits.

## Topic Branches

Git branches are "cheap." Creating branches in Git is incredibly easy and it's an ideal way to isolate a specific set of changes. By keeping a specific set of changes isolated, it will help us to navigate your fork and apply only the changes we're interested in. You should create a clean branch based on the latest spree/master when doing this. It is important you follow these steps exactly, it will prevent you from accidentally including unrelated changes from your local repository into the branch.

For example, if we were submitting a patch to fix an issue with the CSS in the flash error message you could create a branch as follows:

```shell
$ git remote add upstream git://github.com/spree/spree.git
$ git fetch upstream
$ git checkout -b fix-css-for-error-flash --track upstream/master
```

The fetch command will grab all of the latest commits from the Spree master branch. Don't worry, it doesn't permanently alter your working repository and you can return to your master branch later. The track part of the command will tell git that this branch should track with the remote version of the upstream master.  This is another way of saying that the branch should be based on a clean copy of the latest official source code (without any of your unrelated local changes.)

You can then do work locally on this topic branch and push it up to your GitHub fork when you are done. So in our previous example we do something like:

```shell
$ git push origin fix-css-for-error-flash
```

## Commit messages

[Provide solid and clear commit messages](http://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html) so we can read from the commit what is fixed or added in this specific pull request.

When developing in the topic branch it's a best practise to commit a lot with small changes, however some of those commit messages are noise the moment they turn into a pull request. You should rebase and squash the noise commits. For example:

```
- "add store credits"
- "passing specs"
- "forgot a semi-colon"
- "add gift cards"
- "address pr feedback"
```

Rebase and squash this into:

```
- "add store credits"
- "add gift cards"
```

When you are done your work in the topic branch, rebase the topic branch against master (or the stable branch you've forked from)

Sample git rebase:

```shell
git checkout master
git pull --rebase upstream/master
git checkout feature-branch
git rebase -i master
```

This will show you this next screen:

```
pick ce366eb fix typo
pick 59f7318 remove the hub part from the build.sh
pick eaf9993 move this decorator to the correct place again
pick bc39345 add the api refactor to changelogs
pick 87767cf remove the order_decorator from api and added the method in core order model

# Rebase 87a9afd..87767cf onto 87a9afd
#
# Commands:
#  p, pick = use commit
#  r, reword = use commit, but edit the commit message
#  e, edit = use commit, but stop for amending
#  s, squash = use commit, but meld into previous commit
#  f, fixup = like "squash", but discard this commit's log message
#  x, exec = run command (the rest of the line) using shell
#
# These lines can be re-ordered; they are executed from top to bottom.
#
# If you remove a line here THAT COMMIT WILL BE LOST.
#
# However, if you remove everything, the rebase will be aborted.
```

To make this neat you can do something like this:

```
reword ce366eb fix typo
fixup 59f7318 remove the hub part from the build.sh
fixup eaf9993 move this decorator to the correct place again
fixup bc39345 add the api refactor to changelogs
fixup 87767cf remove the order_decorator from api and added the method in core order model

# Rebase 87a9afd..87767cf onto 87a9afd
#
# Commands:
#  p, pick = use commit
#  r, reword = use commit, but edit the commit message
#  e, edit = use commit, but stop for amending
#  s, squash = use commit, but meld into previous commit
#  f, fixup = like "squash", but discard this commit's log message
#  x, exec = run command (the rest of the line) using shell
#
# These lines can be re-ordered; they are executed from top to bottom.
#
# If you remove a line here THAT COMMIT WILL BE LOST.
#
# However, if you remove everything, the rebase will be aborted.
```

The next screen will give you the ability to reword the 5 commits into one neat one.


## For larger pull request create an empty PR with a todo list

[task list](https://help.github.com/articles/writing-on-github/#task-lists)


## What to do when my suggested changes are not accepted?

Since we do not merge new features in the stable branches we suggest that you either
fork the spree repository and merge your changes there, or that you create an extension
that contains the changes you need for the specific branch.
