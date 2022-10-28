# Welcome to husky-java 
[![OpenJDK](https://img.shields.io/badge/openjdk-17-blue)](#)
[![Maven](https://img.shields.io/badge/maven-3.8.3-blue)](#)
[![Node](https://img.shields.io/badge/nodejs-17-blue)](#)
[![License: ISC](https://img.shields.io/badge/License-ISC-yellow.svg)](#)
[![Conventional Commits](https://img.shields.io/badge/Conventional%20Commits-1.0.0-%23FE5196?logo=conventionalcommits&logoColor=white)](https://conventionalcommits.org)

> Proof of Concept of using Husky in a Java project with Maven

## Install

```sh
npm install
```

## Usage

### Commitzen

In order to use Commitzen to aid you write your commits following the [Conventional Commit Standards](https://www.conventionalcommits.org/en/v1.0.0/#summary) you just need type:
```sh
git commit
```

The following selection options will appear on CLI and you just need to follow the steps
![commitzen](./docs/img/git-commit-cz.gif)

### CommitLint

In case you already know the [Conventional Commit Standards](https://www.conventionalcommits.org/en/v1.0.0/#summary), just write your commit, when you finish it, husky will run CommitLint in your commit to check if it is following the standads.

```sh
git commit -m "message not following conventional commit standrds"
```

![commitlint](./docs/img/git-commit-lint.gif)

### Other Checks

It is possible to configure several other hooks.

In this project there is only a git push hook besides the commit check that will run build and tests of java project.

```
git push
```

![push](./docs/img/git-push.gif)

## Run tests

```sh
npm run test
```

## Author

👤 **Bruno Habermann**

* Github: [@bhabermann](https://github.com/bhabermann)
* LinkedIn: [@brunohabermann](https://linkedin.com/in/brunohabermann)

## Show your support

Give a ⭐️ if this project helped you!


***
_This README was generated with ❤️ by [readme-md-generator](https://github.com/kefranabg/readme-md-generator)_