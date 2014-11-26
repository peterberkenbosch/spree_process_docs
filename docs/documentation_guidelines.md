# Documentation Guidelines

Improvements to the documentation are encouraged. The primary source of documentation are the [guides](http://guides.spreecommerce.com). You may make edits to the guide in your fork and then pull request for them to be updated to this site.

The documentation in located in the guides folder on the spree project. To view the documentation localy you can clone the repository and compile the guides using nanoc.

```shell
$ git clone git://github.com/spree/spree.git
$ cd spree/guides
$ bundle install
$ bundle exec nanoc compile
$ bundle exec nanoc view

```
You can then preview the guides in your browser at http://localhost:3000

## Markdown Conventions

It is helpful to standardize some markdown conventions so readers learn to recognize visual cues as they work their way through the documentation and tutorials. Following are the conventions used for the Spree documentation:

## Class Names

When referencing the name of a class, it should be capitalized. If you are writing explanatory prose and not a section of code, the class name should be blocked out with tick (\`) marks. For example:

To begin using your custom `User` class, you must first...

Having the namespace for the class is optional, but should be included when omitting it could cause confusion.

An instance of a class should be lowercase, normal font:

You can view all of the orders for a particular user.

## Buttons, Links, Section Names, Form Elements

These should always reference the correct label and can have their names quoted. Examples:

* Click the "Filter Results" button to update the results.
* Follow the "Stock Transfers" link.
* Information displayed in the "Purchase Funnel" section gives you information...
* If you check "Receive Stock" while creating a new transfer...

## States, Attributes, Methods, Events, and Parameters

When referring to the state of an object - an order, for example - the state name should be lowercase and set off with tick (\`) marks. For example:

Orders that are in the `address` state do not have valid shipping and billing addresses assigned to them yet.

This same style is used for attribute names and their settings, method names, event names, parameter names, parameter settings, and data types.

## Path Names

Path names should be set off with tick (\`) marks, and should include enough of the directory structure to make it clear which file is being referenced. For example:

They are defined in `core/app/models/spree/app_configuration.rb`...

## Adding Emphasis

Any text that needs to be emphasized should be in _italics_.

Only the shipping options in the _shipping_ address are presented.

## Terminal Blocks

You can specify terminal blocks by setting it off with <code>```shell</code>.

In addition, you can differentiate commands you are using from output returned by using the `$` precursor for input and `=>` precursor for output.

```shell
$ irb
$ c = "Hello world"
$ c
=> "Hello world"
```

## Special Blocks

Certain blocks of text can be wrapped in sets of three characters, which will place them in divs with appropriate CSS classes. They are:

```
| *** | Notes.    |
| !!! | Warnings. |
| $$$ | TODO's    |
| --- | A title bar; especially useful for headings for code samples. |
```
