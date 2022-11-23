oclif-hello-world
=================

oclif example Hello World CLI

[![oclif](https://img.shields.io/badge/cli-oclif-brightgreen.svg)](https://oclif.io)
[![Version](https://img.shields.io/npm/v/oclif-hello-world.svg)](https://npmjs.org/package/oclif-hello-world)
[![CircleCI](https://circleci.com/gh/oclif/hello-world/tree/main.svg?style=shield)](https://circleci.com/gh/oclif/hello-world/tree/main)
[![Downloads/week](https://img.shields.io/npm/dw/oclif-hello-world.svg)](https://npmjs.org/package/oclif-hello-world)
[![License](https://img.shields.io/npm/l/oclif-hello-world.svg)](https://github.com/oclif/hello-world/blob/main/package.json)

<!-- toc -->
* [Usage](#usage)
* [Commands](#commands)
<!-- tocstop -->
# Usage
<!-- usage -->
```sh-session
$ npm install -g jsobfuscate
$ jsobfuscate COMMAND
running command...
$ jsobfuscate (--version)
jsobfuscate/0.0.0 darwin-arm64 node-v16.18.0
$ jsobfuscate --help [COMMAND]
USAGE
  $ jsobfuscate COMMAND
...
```
<!-- usagestop -->
# Commands
<!-- commands -->
* [`jsobfuscate hello PERSON`](#jsobfuscate-hello-person)
* [`jsobfuscate hello world`](#jsobfuscate-hello-world)
* [`jsobfuscate help [COMMAND]`](#jsobfuscate-help-command)
* [`jsobfuscate plugins`](#jsobfuscate-plugins)
* [`jsobfuscate plugins:install PLUGIN...`](#jsobfuscate-pluginsinstall-plugin)
* [`jsobfuscate plugins:inspect PLUGIN...`](#jsobfuscate-pluginsinspect-plugin)
* [`jsobfuscate plugins:install PLUGIN...`](#jsobfuscate-pluginsinstall-plugin-1)
* [`jsobfuscate plugins:link PLUGIN`](#jsobfuscate-pluginslink-plugin)
* [`jsobfuscate plugins:uninstall PLUGIN...`](#jsobfuscate-pluginsuninstall-plugin)
* [`jsobfuscate plugins:uninstall PLUGIN...`](#jsobfuscate-pluginsuninstall-plugin-1)
* [`jsobfuscate plugins:uninstall PLUGIN...`](#jsobfuscate-pluginsuninstall-plugin-2)
* [`jsobfuscate plugins update`](#jsobfuscate-plugins-update)

## `jsobfuscate hello PERSON`

Say hello

```
USAGE
  $ jsobfuscate hello [PERSON] -f <value>

ARGUMENTS
  PERSON  Person to say hello to

FLAGS
  -f, --from=<value>  (required) Who is saying hello

DESCRIPTION
  Say hello

EXAMPLES
  $ oex hello friend --from oclif
  hello friend from oclif! (./src/commands/hello/index.ts)
```

_See code: [dist/commands/hello/index.ts](https://github.com/jrgochan/jsobfuscate/blob/v0.0.0/dist/commands/hello/index.ts)_

## `jsobfuscate hello world`

Say hello world

```
USAGE
  $ jsobfuscate hello world

DESCRIPTION
  Say hello world

EXAMPLES
  $ jsobfuscate hello world
  hello world! (./src/commands/hello/world.ts)
```

## `jsobfuscate help [COMMAND]`

Display help for jsobfuscate.

```
USAGE
  $ jsobfuscate help [COMMAND] [-n]

ARGUMENTS
  COMMAND  Command to show help for.

FLAGS
  -n, --nested-commands  Include all nested commands in the output.

DESCRIPTION
  Display help for jsobfuscate.
```

_See code: [@oclif/plugin-help](https://github.com/oclif/plugin-help/blob/v5.1.19/src/commands/help.ts)_

## `jsobfuscate plugins`

List installed plugins.

```
USAGE
  $ jsobfuscate plugins [--core]

FLAGS
  --core  Show core plugins.

DESCRIPTION
  List installed plugins.

EXAMPLES
  $ jsobfuscate plugins
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v2.1.7/src/commands/plugins/index.ts)_

## `jsobfuscate plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ jsobfuscate plugins:install PLUGIN...

ARGUMENTS
  PLUGIN  Plugin to install.

FLAGS
  -f, --force    Run yarn install with force flag.
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Installs a plugin into the CLI.
  Can be installed from npm or a git url.

  Installation of a user-installed plugin will override a core plugin.

  e.g. If you have a core plugin that has a 'hello' command, installing a user-installed plugin with a 'hello' command
  will override the core plugin implementation. This is useful if a user needs to update core plugin functionality in
  the CLI without the need to patch and update the whole CLI.


ALIASES
  $ jsobfuscate plugins add

EXAMPLES
  $ jsobfuscate plugins:install myplugin 

  $ jsobfuscate plugins:install https://github.com/someuser/someplugin

  $ jsobfuscate plugins:install someuser/someplugin
```

## `jsobfuscate plugins:inspect PLUGIN...`

Displays installation properties of a plugin.

```
USAGE
  $ jsobfuscate plugins:inspect PLUGIN...

ARGUMENTS
  PLUGIN  [default: .] Plugin to inspect.

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Displays installation properties of a plugin.

EXAMPLES
  $ jsobfuscate plugins:inspect myplugin
```

## `jsobfuscate plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ jsobfuscate plugins:install PLUGIN...

ARGUMENTS
  PLUGIN  Plugin to install.

FLAGS
  -f, --force    Run yarn install with force flag.
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Installs a plugin into the CLI.
  Can be installed from npm or a git url.

  Installation of a user-installed plugin will override a core plugin.

  e.g. If you have a core plugin that has a 'hello' command, installing a user-installed plugin with a 'hello' command
  will override the core plugin implementation. This is useful if a user needs to update core plugin functionality in
  the CLI without the need to patch and update the whole CLI.


ALIASES
  $ jsobfuscate plugins add

EXAMPLES
  $ jsobfuscate plugins:install myplugin 

  $ jsobfuscate plugins:install https://github.com/someuser/someplugin

  $ jsobfuscate plugins:install someuser/someplugin
```

## `jsobfuscate plugins:link PLUGIN`

Links a plugin into the CLI for development.

```
USAGE
  $ jsobfuscate plugins:link PLUGIN

ARGUMENTS
  PATH  [default: .] path to plugin

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Links a plugin into the CLI for development.
  Installation of a linked plugin will override a user-installed or core plugin.

  e.g. If you have a user-installed or core plugin that has a 'hello' command, installing a linked plugin with a 'hello'
  command will override the user-installed or core plugin implementation. This is useful for development work.


EXAMPLES
  $ jsobfuscate plugins:link myplugin
```

## `jsobfuscate plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ jsobfuscate plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ jsobfuscate plugins unlink
  $ jsobfuscate plugins remove
```

## `jsobfuscate plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ jsobfuscate plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ jsobfuscate plugins unlink
  $ jsobfuscate plugins remove
```

## `jsobfuscate plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ jsobfuscate plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ jsobfuscate plugins unlink
  $ jsobfuscate plugins remove
```

## `jsobfuscate plugins update`

Update installed plugins.

```
USAGE
  $ jsobfuscate plugins update [-h] [-v]

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Update installed plugins.
```
<!-- commandsstop -->
