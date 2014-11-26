## Overview

Spree is an open source project. Anyone can use the code, but more importantly, anyone can contribute. This is a group effort and we value your input. Please consider making a contribution to help improve the Spree project. This guide covers:

* How to file a ticket when you discover a bug
* How to contribute fixes and improvements to the core
* Information on how to improve the documentation

### Who can contribute?

Spree is an open source project and as such contributions are always welcome. Our community is one which encourages involvement from all developers regardless of their ability level. We ask that you be patient with the other members of the community and maintain a respectful attitude towards other people's work. Open source is a great way to learn a new technology so don't be afraid to jump right in, even if you are new to Ruby/Rails.

### Before you contribute

Open source projects tend to be a collaborative effort. Since many people are relying upon Spree for their real world applications, changes to the code can have major implications. Before you write a bug fix or code a new feature, you should find out if anybody is interested in your proposed change. You may find that the thing you're trying to "fix" is actually desired behavior. You might also discover that someone else is working on it. Either way you can save yourself valuable time by announcing your intentions before starting work.

#### Mailing List

One of the best places for communication is the [spree-user mailing list](http://groups.google.com/group/spree-user). You can search this list of previous discussions and get a sense for whether you're trying to address something new.

#### IRC

There is a #spree chat room on the irc.freenode.net network. Sometimes the core contributors hang out there and you can get some feedback on your idea. More information on how to connect is on our [blog](http://spreecommerce.com/blog/irc-101).

!!!
The #spree chat room is not monitored as carefully as the mailing list. Sometimes you'll get lucky and someone will answer your question but we can't provide real time responses to everyone with a question/problem/idea. The mailing list is a much better way to communicate, and it gives everyone the chance to provide a thoughtful response. It's also more permanent than anything discussed on IRC.
!!!

#### Notification via GitHub Issues

You can also search existing bug reports/issues and file a new one if you do not find an issue relevant to your proposed change. See [Filing an Issue](#filing-an-issue) for more details.

***
_The important thing is that you communicate your intention in advance of doing a lot of work. Simple bug fixes and non-controversial changes do not require this approach but you can save some time by suggesting an improvement and having it rejected before you write a bunch of the code._
***

### [Filing an Issue](filing_issue_guide.md)

#### Providing a Pull Request

If you are filing an issue and supplying a patch at the same time, please file a ["Pull Request"](#creating-a-pull-request) instead. The pull request will also create an issue at the same time but it's superior to just creating an issue because the code and issue can be linked.

If the ticket already exists, however, and you want to supply a patch after the fact, you can simply reference the issue number in your commit message. For example, if your commit fixed issue #123 you could use the following commit message:

Fixed a problem with Facebook authentication.

[Fixes #123]

GitHub will automatically detect this commit message when you push it and link the issue. Please see the detailed [GitHub Issues](https://github.com/blog/831-issues-2-0-the-next-generation) blog post for more details.

We add code from Pull Requests to spree using the [hub gem](https://github.com/defunkt/hub), in particular the `hub am` command, which is used like this:

```bash
$ hub am -3 https://github.com/spree/spree/pull/<number>
```

This command will apply the commits from the pull request to the current branch, using a 3-way merge as a fallback. This means that we can run this command in order to apply the patch to different branches. A pull request applied in this way leads to tidier commit history, with no merge commits visible.

***
For this reason, there is no need to create multiple pull requests for Spree's different branches. Please only create one pull request per change and simply mention inside the pull request that it can apply to multiple branches. If a patch does not apply cleanly to a branch, the Spree team may ask you for another one which applies to the other branch.
***

### Feature Requests

We're interested in hearing your ideas for new features but creating feature requests in the Issue Tracker is not the proper way to ask for a feature. A feature request is any idea you have to improve the software experience that is not strictly related to a bug or error of omission.

***
Feature requests that are accompanied by source code are always welcome. In this case you should read the next section on [creating a pull request](#creating-a-pull-request).
***

!!!
Feature requests without accompanying code will be closed immediately. We simply cannot respond efficiently to feature requests through our Issue Tracker. If you want to suggest a feature, please use the [mailing list](http://groups.google.com/group/spree-user).
!!!

### Creating a Pull Request

If you are going to contribute code to the Spree project, the best mechanism for doing this is to create a pull request in GitHub. If you're unfamiliar with the general concept of pull requests you may want to read more on [pull requests in GitHub](https://help.github.com/articles/using-pull-requests).

***
If your code is associated with an existing issue then you can [provide a patch](#providing-a-patch) instead of creating a pull request.
***

#### Creating a Fork

The official Spree source code is maintained in GitHub under the [spree/spree](https://github.com/spree/spree) project. There is a [core team](http://spreecommerce.com/core_team) of developers who are responsible for maintaining the quality of the source code. Your changes will ultimately need to be merged into the official project by a core member.

Thanks to [GitHub](https://github.com/), however, you do not have to wait for a core member to get started with your fix. You simply need to "fork" the project and then start hacking.

***
See the GitHub guide on [creating forks](https://help.github.com/articles/fork-a-repo) for more details.
***




### Contributing to the Documentation

Improvements to the documentation are encouraged. The primary source of documentation are the guides (_HINT: You are reading one now._). You may make edits to the guide in your fork and then pull request for them to be updated to this site.

To build the documentation normally simply clone and install.

```bash
$ git clone git://github.com/spree/spree.git
$ cd spree/guides
$ bundle install
$ bundle exec guides build
```

Then simply use the nanoc command to compile and preview the guides in your browser at http://localhost:3000

```bash
$ nanoc compile
$ nanoc view
```

### Markdown Conventions

It is helpful to standardize some markdown conventions so readers learn to recognize visual cues as they work their way through the documentation and tutorials. Following are the conventions used for the Spree documentation:

####Class Names####

When referencing the name of a class, it should be capitalized. If you are writing explanatory prose and not a section of code, the class name should be blocked out with tick (`) marks. For example:

To begin using your custom `User` class, you must first...

Having the namespace for the class is optional, but should be included when omitting it could cause confusion.

An instance of a class should be lowercase, normal font:

You can view all of the orders for a particular user.

####Buttons, Links, Section Names, Form Elements####

These should always reference the correct label and can have their names quoted. Examples:

* Click the "Filter Results" button to update the results.
* Follow the "Stock Transfers" link.
* Information displayed in the "Purchase Funnel" section gives you information...
* If you check "Receive Stock" while creating a new transfer...

####States, Attributes, Methods, Events, and Parameters####
When referring to the state of an object - an order, for example - the state name should be lowercase and set off with tick (`) marks. For example:

Orders that are in the `address` state do not have valid shipping and billing addresses assigned to them yet.

This same style is used for attribute names and their settings, method names, event names, parameter names, parameter settings, and data types.

####Path Names####
Path names should be set off with tick (`) marks, and should include enough of the directory structure to make it clear which file is being referenced. For example:

They are defined in `core/app/models/spree/app_configuration.rb`...

####Adding Emphasis####
Any text that needs to be emphasized should be in _italics_.

Only the shipping options in the _shipping_ address are presented.

####Terminal Blocks####
You can specify terminal blocks by setting it off with <code>```bash</code>. In addition, you can differentiate commands you are using from output returned by using the `$` precursor for input and `=>` precursor for output.

```bash
$ irb
$ c = "Hello world"
$ c
=> "Hello world"
```

####Special Blocks####

Certain blocks of text can be wrapped in sets of three characters, which will place them in divs with appropriate CSS classes. They are:

| *** | Notes. |
| !!! | Warnings. |
| $$$ | TODO's |
| --- | A title bar; especially useful for headings for code samples. |
