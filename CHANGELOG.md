# Changelog

All notable changes to this project will be documented in this file. See [standard-version](https://github.com/conventional-changelog/standard-version) for commit guidelines.

## 0.1.0 (2019-07-31)

This release marks the begin of tanka's history :tada:!

As of now, tanka aims to nearly seemlessly connect to the point where [ksonnet](https://github.com/ksonnet/ksonnet) left.
The current feature-set is basic, but usable: The three main workflow commands are available (`show`, `diff`, `apply`), environments are supported, code-sharing is done using [`jb`](https://github.com/jsonnet-bundler/jsonnet-bundler).

Stay tuned!

### Features

* **kubernetes:** Show ([7c4bee8](https://github.com/tbraack/tanka/commit/7c4bee8)): Equivalent to `ks show`, allows previewing the generated yaml.
* **kubernetes:** Diff ([a959f38](https://github.com/tbraack/tanka/commit/a959f38)): Uses the `kubectl diff` to obtain a sanitized difference betweent the current and the desired state. Requires Kubernetes 1.13+
* **kubernetes:** Apply ([8fcb4c1](https://github.com/tbraack/tanka/commit/8fcb4c1)): Applies the changes to the cluster (like `ks apply`)
* **kubernetes:** Apply approval ([4c6414f](https://github.com/tbraack/tanka/commit/4c6414f)): Requires a typed `yes` to apply, gives the user the chance to verify cluster and context.
* **kubernetes:** Smart context ([2b3fd3c](https://github.com/tbraack/tanka/commit/2b3fd3c)): Infers the correct context from the `spec.json`. Prevents applying the correct config to the wrong cluster.
* Init Command ([ff8857c](https://github.com/tbraack/tanka/commit/ff8857c)): Initializes a new repository with the suggested directory structure.