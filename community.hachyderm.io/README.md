# Hachyderm Community Resources Website

Here is the static website that is hosted at [community.hachyderm.io](https://community.hachyderm.io).

### Building The Website

Clone the repository and build the submodule.

```
git clone git@github.com:hachyderm/community.git
cd community/community.hachyderm.io
make submodule
```

### Running The Website

The site is built with [Hugo](https://gohugo.io/). You'll need it in order to work on the site. [Installation instructions are here](https://gohugo.io/installation/)

Once you have hugo, run the following command in the `community/community.hachyderm.io` directory to start the development server.

```
make dev
```

The first time you run the command will take a little bit while it downloads some necessities. Once it's running, the dev site is available at [localhost:1313](http://localhost:1313/).

You should not use Docker to locally work on the Community Docs,
only Hugo.

### Adding a new doc page to the web site

Since this site is a Documentation site rather than a blog, using
`hugo new` doesn't work quite as expected. Instead, we recommend
making a new file and including the following header at the top:

```
---
title: "Your Title Goes Here"
linkTitle: "YourLinkTitleGoesHere"
weight: 4
description: >
  Your single or multiline description goes here.
---

Your content goes here.
```

All of our docs are going into English first, but may be
translated into other languages. To create the file in the correct
file path:

1. All documentation files should be in the `content/en/docs`
parent directory.
1. In order to create a new doc for the parent level of the
left navigation panel, then the file should be in
`content/en/docs/$NEWPARENTDIR/_index.md`
1. If you are planning to add sub-items to an existing parent
level menu item, then it should be in
`content/en/docs/$EXISTINGPARENTDIR/filename.md`
1. Note all `$PARENTDIR` require a minimum of an `_index.md` file.


The `weight` field determines what order the menu items appear on the
nav menu. By default, all files with the same `weight` are
alphabetized. All files added to the parent nav menu should have a
`weight: 4` and all sub-items should have a `weight: 20`. (See the
`infrastructure` and `accounts` files for reference.)

### Contributing to the web site

As we are migrating to our new site all changes must be
non-destructive. This means that as we move a doc from `DocFile.md`
in the parent directory the Markdown file must not be deleted as
part of the migration to minimize breaking existing links until
all existing documentation is in the community site.

New documentation pages should be added directly to the Community
site itself.
