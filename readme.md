# requirebin

create programs in the browser using modules from NPM

[![js-standard-style](https://raw.githubusercontent.com/feross/standard/master/badge.png)](https://github.com/feross/standard)

[![Build Status](https://travis-ci.org/maxogden/requirebin.svg?branch=master)](https://travis-ci.org/maxogden/requirebin)

the app itself is 100% client side (requirebin.com is hosted on github pages) but it relies on these three APIs:

- https://github.com/substack/node-browserify
- https://github.com/jesusabdullah/browserify-cdn
- https://github.com/prose/gatekeeper (only necessary if you want to publish gists)

both can be hosted anywhere, the instances used by requirebin.com are hosted on a linode VPS and nodejitsu, respectively.

by default `config.js` is set to use `http://localhost:8000` as the browserify-cdn endpoint but feel free to use `http://wzrd.in` which is the one I host on a VPS (requires internet connection to use but hey)

## getting it to run locally

### set up browserify-cdn

```
npm install -g browserify
npm install -g browserify-cdn
browserify-cdn 8000
```

### set up gatekeeper (only if you want to publish gists in dev mode)

1. make a new github oauth application and set the app URL and callback URL to `http://localhost:5000`
2. [follow these instructions](https://github.com/prose/gatekeeper#setup-your-gatekeeper) to install and start gatekeeper on port 9999

### edit `config.js` to point to your endpoints

```
npm install
npm start
open http://localhost:5000
```

### deploying

if you are a collaborator and want to deploy code to `requirebin.com`, simply run `npm run deploy`

### contributing

requirebin is an **OPEN Open Source Project**. This means that:

> Individuals making significant and valuable contributions are given commit-access to the project to contribute as they see fit. This project is more like an open wiki than a standard guarded open source project.

See the [CONTRIBUTING.md](contributing.md) file for more details.

## Collaborators

requirebin is only possible due to the excellent work of the following collaborators:

<table><tbody><tr><th align="left">maxogden</th><td><a href="https://github.com/maxogden">GitHub/maxogden</a></td></tr>
<tr><th align="left">h0ke</th><td><a href="https://github.com/h0ke">GitHub/h0ke</a></td></tr>
<tr><th align="left">kumavis</th><td><a href="https://github.com/kumavis">GitHub/kumavis</a></td></tr>
<tr><th align="left">maurizzzio</th><td><a href="https://github.com/maurizzzio">GitHub/maurizzzio</a></td></tr>
</tbody></table>

## license

BSD
