# Hachyderm Community Resources Website

This is the source code for the
[community.hachyderm.io](https://community.hachyderm.io) website.

## Contributing To The Website

Contributions to the website are welcome. Pull requests 
can be made on the
[primary hachyderm community repo](https://github.com/hachyderm/community/).

### Forking And Pull Requests

The website is part of the overall 
[hachyderm community project repo](https://github.com/hachyderm/community).
Contributions are made by through the standard
fork and pull request (PR) process. Details on that
process are here:

[GitHub - Contributing To Projects](https://docs.github.com/en/get-started/quickstart/contributing-to-projects)

### Re-Syncing Your Fork

Changed made to the primary hachyderm/community repo
don't get synced to your forked version automatically.
A re-sync is required when you're ready to make more 
changes. Details on that can be found here:

[GitHub - Syncing A Fork](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/syncing-a-fork)

Once the sync is done, create a new branch from
the freshly updated `main` branch and continue
through the pull request process as before.

## Working On The Site

The website is built with the [Hugo](https://gohugo.io/)
static site generator. Besides git, it's the only
prerequisite you'll need to work on the site.

(Note: If you're on a Mac, Xcode may also be
required.)

### Installing Hugo

Details for installing hugo are here:

[Hugo - Installation](https://gohugo.io/installation/)

### Building The Website

The website requires an initial build process after 
you clone it to your local machine. Inside the repo, 
move into the `community.hachyderm.io` directory on 
the command line and make the submodule with: 

```
cd community.hachyderm.io

make submodule
```

That process will take a little time as it pulls down 
all the parts it needs.

### Running The Website On localhost

Once everything is built, start a local development
version of the site by running this command in
the `community.hachyderm.io` directory.

```
make dev
```

The first time you run the command will take a little 
bit while it downloads some necessities. Once it's 
running, the dev site is available at 
[localhost:1313](http://localhost:1313/).

### Introduction To Hugo 

If you've never worked with Hugo before, these
pages from the Hugo Getting Started section
are worth a look:

[Hugo - Quick Start](https://gohugo.io/getting-started/quick-start/)

[Hugo - Basic Usage](https://gohugo.io/getting-started/usage/)

[Hugo - Directory Structure](https://gohugo.io/getting-started/directory-structure/)

They'll show you the lay of the land so you can
get started contributing.

### Issues

There is a general issue tracker for the community. 
Use it for communications rather than pinging
the admins directly on Mastodon:

[Hachyderm Community Issue Tracker](https://github.com/hachyderm/community/issues)

### Happy Hachyderming

Thanks for your help maintaining and improving the
community!

