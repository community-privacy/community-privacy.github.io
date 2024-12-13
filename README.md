# Community Privacy

Website for Community Privacy.

Site uses [al-folio](https://github.com/alshedivat/al-folio) template.

## Setup

1. Clone repo

```
$ git clone git@github.com:community-privacy/community-privacy.github.io.git
```

As of 12/13/24, there is an [error](https://github.com/alshedivat/al-folio/issues/2880) with the docker image, so we will use the local setup:

```
$ bundle install
# assuming pip is your Python package manager
$ pip install jupyter
$ bundle exec jekyll serve
```

Open your browser and go to `http://localhost:4000`.

For additional installation and deployment details please refer to [INSTALL.md](INSTALL.md).

## Pushing Changes

Before pushing changes:

```
# Lint and prettify code
$ npx prettier --write .
```
