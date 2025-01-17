EN | [RU](README-RU.md)

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)

![badge-jvm](http://img.shields.io/badge/platform-jvm-DB413D.svg?style=flat)
![badge-android](http://img.shields.io/badge/platform-android-6EDB8D.svg?style=flat)
![badge-ios](http://img.shields.io/badge/platform-ios-lightgray?style=flat)

# Overview
## What is Monadic
Monadic is a distributed Kotlin multiplatform library that provides the ability to use functional programming in Kotlin.

### What is distributed framework
Monadic allows you to include in dependencies only the part that you plan to use in the project.

Developers often do not add large functional libraries to their projects due to excessive workload,
increasing the size of the application and the possibility for other developers to use the unwanted part of the library.

Monadic solves this problem - connect only those parts of the library that you plan to use.

# How to use
## Using the BOM
![Maven Central](https://img.shields.io/maven-central/v/io.github.pavelannin/monadic-bom?label=monadic-bom)

The `BOM` specification allows you to manage all versions of the Monadic library by specifying only the version of the specification.
The specification itself contains links to versions of various Monadic libraries. When using the specification in your application ,
you do not need to add any version of the Monadic library dependency. When you update a version of the specification,
all the libraries you use are automatically updated to the new versions.

It is recommended to use the `BOM` specification if you use more than one part of the Monadic library.

```gradle
implementation(platform("io.github.pavelannin:monadic-bom:<version>"))
```

## Checkable
![Maven Central](https://img.shields.io/maven-central/v/io.github.pavelannin/monadic-checkable-core?label=monadic-checkable-core)

The `Checkable` type is a functional construct used to extend the any type with states: checked (marked)
or Unchecked.

`Checkable` is convenient to use at the level of business logic and application view states.

```gradle
implementation("io.github.pavelannin:monadic-checkable-core")
```

## Either
![Maven Central](https://img.shields.io/maven-central/v/io.github.pavelannin/monadic-either-core?label=monadic-either-core)

The `Either` monad is a functional construct used to handle alternative results or errors.

Typed errors refer to a functional programming technique in which potential errors
that may occur during the execution of an operation are explicitly described in the signature.

```gradle
implementation("io.github.pavelannin:monadic-either-core")
```

## Utility functions
![Maven Central](https://img.shields.io/maven-central/v/io.github.pavelannin/monadic-function-core?label=monadic-function-core)

Utilities for functions in a functional style: composition, currying, etc.

```gradle
implementation("io.github.pavelannin:monadic-function-core")
```

## Identifiable
![Maven Central](https://img.shields.io/maven-central/v/io.github.pavelannin/monadic-identifiable-core?label=monadic-identifiable-core)

The `Identifiable` type is a universal design designed for identification types. 
Used to add a typed identifier to type.

```gradle
implementation("io.github.pavelannin:monadic-identifiable-core")
```

## LCE
![Maven Central](https://img.shields.io/maven-central/v/io.github.pavelannin/monadic-lce-core?label=monadic-lce-core)

The `LCE` monad is a functional construct used to handle the state of operations (consisting of 3 states: execution,
successful and error).

Convenient use for determining the state of the screen or an operation on a user view
(used in MVI approaches).

```gradle
implementation("io.github.pavelannin:monadic-lce-core")
```

### LCE - Either (Extensions)
![Maven Central](https://img.shields.io/maven-central/v/io.github.pavelannin/monadic-lce-either?label=monadic-lce-either)

A set of utilities that extend the capabilities of `LCE` and `Either`.

```gradle
implementation("io.github.pavelannin:monadic-lce-either")
```

### LCE - Result (Extensions)
![Maven Central](https://img.shields.io/maven-central/v/io.github.pavelannin/monadic-lce-result?label=monadic-lce-result)

A set of utilities that extend the capabilities of `LCE` and `Result`.

```gradle
implementation("io.github.pavelannin:monadic-lce-result")
```

## Optional
![Maven Central](https://img.shields.io/maven-central/v/io.github.pavelannin/monadic-optional-core?label=monadic-optional-core)

The `Optinal` monad is a functional construct used for a value that can be `null'.

```gradle
implementation("io.github.pavelannin:monadic-optional-core")
```

### Optional - Either (Extensions)
![Maven Central](https://img.shields.io/maven-central/v/io.github.pavelannin/monadic-optional-either?label=monadic-optional-either)

A set of utilities that extend the capabilities of `Optional` and `Either'.

```gradle
implementation("io.github.pavelannin:monadic-optional-either")
```

## Refreshable
![Maven Central](https://img.shields.io/maven-central/v/io.github.pavelannin/monadic-refreshable-core?label=monadic-refreshable-core)

The `Refreshable` type is a functional construct used to extend the any type with states:
refreshing or refreshed.

`Refreshable` is convenient to use at the level of business logic and application view states.

```gradle
implementation("io.github.pavelannin:monadic-refreshable-core")
```

## Result
![Maven Central](https://img.shields.io/maven-central/v/io.github.pavelannin/monadic-result-core?label=monadic-result-core)

The `Result` monad is a functional construct that represents success (`Result.OK`) or failure (`Result.Error`]).

```gradle
implementation("io.github.pavelannin:monadic-result-core")
```
