# ddft.wiki

Source code for ddft.wiki. We use a system called [Cryogen](https://cryogenweb.org) to generate the site. A quick overview is here.

## To build locally

```bash

lein run

```

## To test locally

```bash

lein ring server

```

## Deployment to ddft.wiki

[![CircleCI](https://circleci.com/gh/ddftwiki/ssg/tree/master.svg?style=svg)](https://circleci.com/gh/ddftwiki/ssg/tree/master)

When we push changes to the `master` branch of this repository, an automatic build is kicked off via [CircleCI](https://circleci.com/gh/ddftwiki/ssg). This executes `lein run` and then pushes the resulting files to our ddftwiki/ddftwiki.github.io repo. This causes github pages (who hosts the site backing ddft.wiki) to publish a new version of our site. 

## Configuration

The config file is at `resources/templates/config.edn1`. This controls some misc SSG stuff. You shouldn't need to modify this.

## Templates

You can find templates at `resources/templates/themes/ddftwiki/`. They use [Selmer](https://github.com/yogthos/Selmer) for a (a django/jinja/liquid/twig-style) templating system. Look at the examples and ask emidln if you have questions.

## Markdown

For basic syntax and a test console, see: https://rawgit.com/yogthos/markdown-clj/master/demo/markdown.html 

For our actual implementation, see: https://github.com/yogthos/markdown-clj.

## Pages

You can find pages at `resources/templates/md/pages/`. They are written in Markdown.

## Posts

You can find blog posts at `resources/templates/md/posts/`. They are written in Markdown.


# License

## Content

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

The website content of this project is licensed under the Creative Commons Attribution 4.0 as found in the LICENSE.content file.

## Code

[![License](https://img.shields.io/badge/License-EPL%201.0-red.svg)](https://opensource.org/licenses/EPL-1.0)

The software source code of this project is licensed under the Eclipse Public License 1.0 as found in the LICENSE.code file.
