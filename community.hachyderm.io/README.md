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
