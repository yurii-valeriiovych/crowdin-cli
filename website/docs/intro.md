---
slug: /
---

# Introduction

Welcome to the official documentation site for Crowdin CLI - a powerful command-line tool that simplifies the management of your localization projects on Crowdin. With Crowdin CLI, you can easily upload source files, download translations, and keep your localized content up-to-date with just a few simple commands.

So, whether you're looking to streamline your localization process, improve your team's collaboration, or simply save time and effort, Crowdin CLI is the tool for you.

- Automate the process of updating your source files in your Crowdin project
- Download translations from Crowdin and automatically save them in the correct locations
- Upload all your existing translations to Crowdin in minutes

This is a cross-platform, and it runs in a terminal on Linux based and macOS operating systems or in Command Prompt on Windows

[![Docker Pulls](https://img.shields.io/docker/pulls/crowdin/cli?logo=docker&cacheSeconds=2000)](https://hub.docker.com/r/crowdin/cli)
[![npm](https://img.shields.io/npm/dt/@crowdin/cli?logo=npm&cacheSeconds=2000)](https://www.npmjs.com/package/@crowdin/cli)
[![homebrew downloads](https://img.shields.io/homebrew/installs/dy/crowdin?logo=homebrew)](https://formulae.brew.sh/formula/crowdin)
[![GitHub contributors](https://img.shields.io/github/contributors/crowdin/crowdin-cli?cacheSeconds=1000)](https://github.com/crowdin/crowdin-cli/graphs/contributors)
[![codecov](https://codecov.io/gh/crowdin/crowdin-cli/branch/cli3/graph/badge.svg)](https://codecov.io/gh/crowdin/crowdin-cli)
![GitHub](https://img.shields.io/github/license/crowdin/crowdin-cli?cacheSeconds=50000)
[![GitHub Repo stars](https://img.shields.io/github/stars/crowdin/crowdin-cli?style=social&cacheSeconds=1800)](https://github.com/crowdin/crowdin-cli/stargazers)

<iframe width="100%" height="500px" src="https://www.youtube.com/embed/0duN4khpWjM" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen=""></iframe>

## Features

- Interactive generation of a configuration file
- Upload source files and existing translations to a Crowdin project
- Download the latest translations from Crowdin to the specified place
- Multithreading for source and translation files upload
- Show translation and proofreading progress for a project
- Manage source strings in a Crowdin project
- Manage glossaries and translation memories
- Manage tasks in a Crowdin project
- Manage source files and branches in the current project
- Run Pre-Translation
- Bash/Zsh command completion
- Process indicators, loading states, emojis
- HTTP Proxy support including authorization
- and more.

## Running

Use the following command to run the app:

```bash
crowdin
```
Alternative method:

```bash
java -jar crowdin-cli.jar
```

## Requirements

Check that you have Java 8 or newer installed. Type `java -version` command in the terminal (Command Prompt on Windows) to check Java version. For example, java version "1.8.0_212" means that you have Java 8 Update 212 installed.

If you don’t have Java installed, download it from [Oracle’s website](https://www.java.com/en/).

## Further Reading

- [Installation](/installation)
- [Configuration](/configuration)
- [Commands](/commands/crowdin)