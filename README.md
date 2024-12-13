# Community Privacy

Website for Community Privacy. Site uses [al-folio](https://github.com/alshedivat/al-folio) template. 

`$ bundle exec jekyll serve` to run locally. 

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

### Code quality checks

Currently, we run some checks to ensure that the code quality and generated site are good. The checks are done using GitHub Actions and the following tools:

- [Prettier](https://prettier.io/) - check if the formatting of the code follows the style guide
- [lychee](https://lychee.cli.rs/) - check for broken links
- [Axe](https://github.com/dequelabs/axe-core) (need to run manually) - do some accessibility testing

To set these up:

[Prettier](https://prettier.io/):
```
$ npm install --save-dev --save-exact prettier # Install prettier
$ npx prettier . --write # Run prettier
```

[lychee](https://lychee.cli.rs/): (This took too long to install for me lol so I skipped it personally... -RW)
```
$ brew install lychee # Install lychee 
$ lychee . # Run lychee 
```

[Axe](https://github.com/dequelabs/axe-core):
```
$ npm install axe-core --save-dev
```

## Dev notes
For searching `"SEARCH TERM"`: (remove quotes) 
```
$ grep -r --exclude-dir=vendor --exclude-dir=_site --exclude-dir=assets --exclude-dir=node_modules --exclude-dir=lighthouse_results "SEARCH TERM"
```

## Pushing Changes

Before pushing changes:

```
# Lint and prettify code
$ npx prettier --write .
```

