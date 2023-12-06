# ChrisJohns.me Blog - A [Jekyll](https://jekyllrb.com) built website

[![pages-build-deployment](https://github.com/ChrisJohns-me/chrisjohns.me/actions/workflows/pages/pages-build-deployment/badge.svg)](https://github.com/ChrisJohns-me/chrisjohns.me/actions/workflows/pages/pages-build-deployment)

## Table of Contents

- [ChrisJohns.me Blog - A Jekyll built website](#chrisjohnsme-blog---a-jekyll-built-website)
  - [Table of Contents](#table-of-contents)
  - [GitHub Pages](#github-pages)
  - [Installation](#installation)
    - [Prerequisites](#prerequisites)
    - [Setup](#setup)
  - [Local Serving](#local-serving)

## GitHub Pages

This site is hosted and deployed by [GitHub Pages](https://pages.github.com).

## Installation

### Prerequisites

- [Visual Studio Code](https://code.visualstudio.com)
- [Jekyll Requirements](https://jekyllrb.com/docs/installation/)
  - [Ruby](https://www.ruby-lang.org/en/downloads/)
  - [RubyGems](https://rubygems.org/pages/download)
  - [GCC](https://gcc.gnu.org/install/) and [Make](https://www.gnu.org/software/make/)
- [GNU coreutils](https://www.gnu.org/software/coreutils/) (if running Debian or macOS)
  - Debian

  ```console
  $ apt-get install coreutils
  ```

  - macOS

  ```console
  $ brew install coreutils
  ```

### Setup

Before running or building for the first time, please complete the installation of the Jekyll plugins. Go to the root directory of project and run:

```console
$ bundle install
```

`bundle` will automatically install all the dependencies specified by `Gemfile`.

## Local Serving

```console
$ bundle exec jekyll serve --livereload
```
