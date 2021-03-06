# dd-trace-js

[![npm](https://img.shields.io/npm/v/dd-trace.svg)](https://www.npmjs.com/package/dd-trace)
[![CircleCI](https://img.shields.io/circleci/project/github/DataDog/dd-trace-js.svg)](https://circleci.com/gh/DataDog/dd-trace-js/tree/master)

**JavaScript APM Tracer (beta)**

This project is in open beta and under active development. Please contact [Datadog support](https://docs.datadoghq.com/help) with any questions.

## Getting Started

For a basic product overview, check out our [setup documentation](https://docs.datadoghq.com/tracing/setup/javascript/).

For installation, configuration, and details about using the API, check out our [API documentation](https://datadog.github.io/dd-trace-js).

For descriptions of terminology used in APM, take a look at the [official documentation](https://docs.datadoghq.com/tracing/visualization/).

## Development

Before contributing to this open source project, read our [CONTRIBUTING.md](https://github.com/DataDog/dd-trace-js/blob/master/CONTRIBUTING.md).

### Requirements

Since this project supports multiple Node versions, using a version
manager such as [nvm](https://github.com/creationix/nvm) is recommended.

To get started once you have a Node version installed, run:

```sh
$ npm install
```

### Testing

Before running the tests, the data stores need to be running.
The easiest way to start all of them is to use the provided
docker-compose configuration:

```sh
$ docker-compose up -d
```

To run the unit tests, use:

```sh
$ npm test
```

To run the unit tests continuously in watch mode while developing, use:

```sh
$ npm run tdd
```

### Linting

We use [ESLint](https://eslint.org) to make sure that new code is
conform to our coding standards.

To run the linter, use:

```sh
$ npm run lint
```

### Continuous Integration

We rely on CircleCI 2.0 for our tests. If you want to test how the CI behaves
locally, you can use the CircleCI Command Line Interface as described here:
https://circleci.com/docs/2.0/local-jobs/

After installing the `circleci` CLI, simply run one of the following:

```sh
$ circleci build --job lint
$ circleci build --job build-node-4
$ circleci build --job build-node-6
$ circleci build --job build-node-8
$ circleci build --job build-node-latest
```

### Benchmarks

When two or more approaches must be compared, please write a benchmark
in the `benchmark/index.js` module so that we can keep track of the
most efficient algorithm. To run your benchmark, just:

```sh
$ npm run bench
```
