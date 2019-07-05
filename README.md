# README

The primary goal of this project is to organize a concerted community effort to improve the ABCI Users Guide that explains how to utilize [AI Bridging Cloud Infrastructure (ABCI)](https://abci.ai/). ABCI is the world's first large-scale Open AI Computing Infrastructure, constructed and operated by [National Institute of Advanced Industrial Science and Technology (AIST)](https://www.aist.go.jp/).  We would welcome your feedbacks including pull requests.

On every *release* we will deploy it as the current *official* version of the ABCI User Guide, which is located at [https://docs.abci.ai/](https://docs.abci.ai/).

## Structure of the repository

This repository consists of the following [MkDocs](https://www.mkdocs.org/) documents:

| Directory | officially deployed URL | Notes |
|:--|:--|:--|
| root/ | https://docs.abci.ai/    | Document root of the ABCI User Guide |
| ja/   | https://docs.abci.ai/ja/ | Japanese version |
| en/   | https://docs.abci.ai/en/ | English version |
| portal/root/ | https://docs.abci.ai/portal/    | Document root of the ABCI Portal Guide |
| portal/ja/   | https://docs.abci.ai/portal/ja/ | Japanese version |
| portal/en/   | https://docs.abci.ai/portal/en/ | English version |

## Development

You can clone the repository to your local environment and run the builtin development server.

```
$ pip install mkdocs
$ pip install mkdocs-material
$ pip install ghp-import
$ git clone https://github.com/aistairc/abci-docs.git
$ cd abci-docs
$ cd root/ or ja/ or en/
$ mkdocs serve
```

And, open 'http://127.0.0.1:8000/' using a web browser.

## Build and deploy

To generate the static versions of documents:

```
$ make -f site.mk
(static files are generated under site/ directory)
```

And, to deploy and publish generated documents to `gh-pages` branch:

```
$ ghp-import -c docs.abci.ai -r origin -b gh-pages -p site
```
