[![Build Status](https://travis-ci.com/pmonks/CLJ-2253.svg?branch=master)](https://travis-ci.com/pmonks/CLJ-2253)
[![Open Issues](https://img.shields.io/github/issues/pmonks/CLJ-2253.svg)](https://github.com/pmonks/CLJ-2253/issues)
[![Average time to resolve an issue](http://isitmaintained.com/badge/resolution/pmonks/CLJ-2253.svg)](http://isitmaintained.com/project/pmonks/CLJ-2253 "Average time to resolve an issue")
[![License](https://img.shields.io/github/license/pmonks/CLJ-2253.svg)](https://github.com/pmonks/CLJ-2253/blob/master/LICENSE)
[![Dependencies Status](https://versions.deps.co/pmonks/CLJ-2253/status.svg)](https://versions.deps.co/pmonks/CLJ-2253)
[![Join the chat at https://gitter.im/CLJ-2253/Lobby](https://badges.gitter.im/CLJ-2253/Lobby.svg)](https://gitter.im/CLJ-2253/Lobby?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

# CLJ-2253

This library implements a workaround for [CLJ-2253](https://dev.clojure.org/jira/browse/CLJ-2253).  Simply require (or use) this namespace before using `slurp` and you're done.

## Installation

CLJ-2253 is available as a Maven artifact from [Clojars](https://clojars.org/org.pmonks/clj-2253).  The latest released version is:

[![Clojars Project](https://img.shields.io/clojars/v/org.clojars.pmonks/clj-2253.svg)](https://clojars.org/org.clojars.pmonks/clj-2253)

### Trying it Out
If you prefer to kick the library's tyres before creating a project, you can use the [`lein try` plugin](https://github.com/rkneufeld/lein-try):

```shell
$ lein try org.clojars.pmonks/clj-2253
```

or, if you have installed the [Clojure CLI tools](https://clojure.org/guides/getting_started#_clojure_installer_and_cli_tools):

```shell
$ clj -Sdeps '{:deps {org.clojars.pmonks/clj-2253 {:mvn/version "#.#.#"}}}'  # Where #.#.# is replaced with an actual version number
```

Either way, you will be dropped in a REPL with the library downloaded and ready for use.

## Usage

The functionality is provided by a single namespace, `CLJ-2253`, that will work its hacky magic as soon as it's loaded.

Require it in the REPL (incl. a `lein try` REPL):

```clojure
(require '[CLJ-2253])
```

Require it in your project:

```clojure
(ns my-app.core
  (:require [CLJ-2253]))
```

## Tested Versions

CLJ-2253 is [tested on](https://travis-ci.com/pmonks/CLJ-2253):

|                           | JVM v1.6        | JVM v1.7       | JVM v1.8 | JVM v9 | JVM v10 | JVM v11 |
|                      ---: |  :---:          |  :---:         |  :---:   |  :---: |  :---:  |  :---:  |
| Clojure 1.5.1             | ❌<sup>†</sup> | ✅             | ✅      | ✅    | ✅      | ✅      |
| Clojure 1.6.0             | ❌<sup>†</sup> | ✅             | ✅      | ✅    | ✅      | ✅      |
| Clojure 1.7.0             | ❌<sup>†</sup> | ✅             | ✅      | ✅    | ✅      | ✅      |
| Clojure 1.8.0             | ❌<sup>†</sup> | ✅             | ✅      | ✅    | ✅      | ✅      |
| Clojure 1.9.0             | ❌<sup>†</sup> | ✅             | ✅      | ✅    | ✅      | ✅      |
| Clojure 1.10.0 (snapshot) | ❌<sup>†</sup> | ❌<sup>‡</sup> | ✅      | ✅    | ✅      | ✅      |

<sup>†</sup> Leiningen v2.8 only supports JVM v1.7 and up

<sup>‡</sup> Clojure v1.10 only supports JVM v1.8 and up

## Contributor Information

[GitHub project](https://github.com/pmonks/CLJ-2253)

[Bug Tracker](https://github.com/pmonks/CLJ-2253/issues)

## License

Copyright 2018 Peter Monks

Distributed under the [Apache License, Version 2.0](http://www.apache.org/licenses/LICENSE-2.0).

SPDX-License-Identifier: [Apache-2.0](https://spdx.org/licenses/Apache-2.0)

### 3rd Party Licenses

To see the full list of licenses of all third party libraries used by this project, please run:

```shell
$ lein licenses :csv | cut -d , -f3 | sort | uniq
```

To see the dependencies and licenses in detail, run:

```shell
$ lein licenses
```
