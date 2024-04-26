oclif-hello-world
<!-- ALL-CONTRIBUTORS-BADGE:START - Do not remove or modify this section -->
[![All Contributors](https://img.shields.io/badge/all_contributors-0-orange.svg?style=flat-square)](#contributors-)
<!-- ALL-CONTRIBUTORS-BADGE:END -->
=================

oclif example Hello World CLI

[![oclif](https://img.shields.io/badge/cli-oclif-brightgreen.svg)](https://oclif.io)
[![GitHub license](https://img.shields.io/github/license/oclif/hello-world)](https://github.com/oclif/hello-world/blob/main/LICENSE)

<!-- toc -->
* [Usage](#usage)
* [Commands](#commands)
<!-- tocstop -->
# Usage
<!-- usage -->
```sh-session
$ npm install -g jeep
$ jeep COMMAND
running command...
$ jeep (--version)
jeep/0.0.1 darwin-arm64 node-v20.12.2
$ jeep --help [COMMAND]
USAGE
  $ jeep COMMAND
...
```
<!-- usagestop -->
# Commands
<!-- commands -->
* [`jeep hello PERSON`](#jeep-hello-person)
* [`jeep hello world`](#jeep-hello-world)
* [`jeep help [COMMAND]`](#jeep-help-command)
* [`jeep plugins`](#jeep-plugins)
* [`jeep plugins add PLUGIN`](#jeep-plugins-add-plugin)
* [`jeep plugins:inspect PLUGIN...`](#jeep-pluginsinspect-plugin)
* [`jeep plugins install PLUGIN`](#jeep-plugins-install-plugin)
* [`jeep plugins link PATH`](#jeep-plugins-link-path)
* [`jeep plugins remove [PLUGIN]`](#jeep-plugins-remove-plugin)
* [`jeep plugins reset`](#jeep-plugins-reset)
* [`jeep plugins uninstall [PLUGIN]`](#jeep-plugins-uninstall-plugin)
* [`jeep plugins unlink [PLUGIN]`](#jeep-plugins-unlink-plugin)
* [`jeep plugins update`](#jeep-plugins-update)

## `jeep hello PERSON`

Say hello

```
USAGE
  $ jeep hello PERSON -f <value>

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

_See code: [src/commands/hello/index.ts](https://github.com/projects/jeep/blob/v0.0.1/src/commands/hello/index.ts)_

## `jeep hello world`

Say hello world

```
USAGE
  $ jeep hello world

DESCRIPTION
  Say hello world

EXAMPLES
  $ jeep hello world
  hello world! (./src/commands/hello/world.ts)
```

_See code: [src/commands/hello/world.ts](https://github.com/projects/jeep/blob/v0.0.1/src/commands/hello/world.ts)_

## `jeep help [COMMAND]`

Display help for jeep.

```
USAGE
  $ jeep help [COMMAND...] [-n]

ARGUMENTS
  COMMAND...  Command to show help for.

FLAGS
  -n, --nested-commands  Include all nested commands in the output.

DESCRIPTION
  Display help for jeep.
```

_See code: [@oclif/plugin-help](https://github.com/oclif/plugin-help/blob/v6.0.21/src/commands/help.ts)_

## `jeep plugins`

List installed plugins.

```
USAGE
  $ jeep plugins [--json] [--core]

FLAGS
  --core  Show core plugins.

GLOBAL FLAGS
  --json  Format output as json.

DESCRIPTION
  List installed plugins.

EXAMPLES
  $ jeep plugins
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.0.15/src/commands/plugins/index.ts)_

## `jeep plugins add PLUGIN`

Installs a plugin into jeep.

```
USAGE
  $ jeep plugins add PLUGIN... [--json] [-f] [-h] [-s | -v]

ARGUMENTS
  PLUGIN...  Plugin to install.

FLAGS
  -f, --force    Force npm to fetch remote resources even if a local copy exists on disk.
  -h, --help     Show CLI help.
  -s, --silent   Silences npm output.
  -v, --verbose  Show verbose npm output.

GLOBAL FLAGS
  --json  Format output as json.

DESCRIPTION
  Installs a plugin into jeep.

  Uses bundled npm executable to install plugins into /Users/dmitrysomov/.local/share/jeep

  Installation of a user-installed plugin will override a core plugin.

  Use the JEEP_NPM_LOG_LEVEL environment variable to set the npm loglevel.
  Use the JEEP_NPM_REGISTRY environment variable to set the npm registry.

ALIASES
  $ jeep plugins add

EXAMPLES
  Install a plugin from npm registry.

    $ jeep plugins add myplugin

  Install a plugin from a github url.

    $ jeep plugins add https://github.com/someuser/someplugin

  Install a plugin from a github slug.

    $ jeep plugins add someuser/someplugin
```

## `jeep plugins:inspect PLUGIN...`

Displays installation properties of a plugin.

```
USAGE
  $ jeep plugins inspect PLUGIN...

ARGUMENTS
  PLUGIN...  [default: .] Plugin to inspect.

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

GLOBAL FLAGS
  --json  Format output as json.

DESCRIPTION
  Displays installation properties of a plugin.

EXAMPLES
  $ jeep plugins inspect myplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.0.15/src/commands/plugins/inspect.ts)_

## `jeep plugins install PLUGIN`

Installs a plugin into jeep.

```
USAGE
  $ jeep plugins install PLUGIN... [--json] [-f] [-h] [-s | -v]

ARGUMENTS
  PLUGIN...  Plugin to install.

FLAGS
  -f, --force    Force npm to fetch remote resources even if a local copy exists on disk.
  -h, --help     Show CLI help.
  -s, --silent   Silences npm output.
  -v, --verbose  Show verbose npm output.

GLOBAL FLAGS
  --json  Format output as json.

DESCRIPTION
  Installs a plugin into jeep.

  Uses bundled npm executable to install plugins into /Users/dmitrysomov/.local/share/jeep

  Installation of a user-installed plugin will override a core plugin.

  Use the JEEP_NPM_LOG_LEVEL environment variable to set the npm loglevel.
  Use the JEEP_NPM_REGISTRY environment variable to set the npm registry.

ALIASES
  $ jeep plugins add

EXAMPLES
  Install a plugin from npm registry.

    $ jeep plugins install myplugin

  Install a plugin from a github url.

    $ jeep plugins install https://github.com/someuser/someplugin

  Install a plugin from a github slug.

    $ jeep plugins install someuser/someplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.0.15/src/commands/plugins/install.ts)_

## `jeep plugins link PATH`

Links a plugin into the CLI for development.

```
USAGE
  $ jeep plugins link PATH [-h] [--install] [-v]

ARGUMENTS
  PATH  [default: .] path to plugin

FLAGS
  -h, --help          Show CLI help.
  -v, --verbose
      --[no-]install  Install dependencies after linking the plugin.

DESCRIPTION
  Links a plugin into the CLI for development.
  Installation of a linked plugin will override a user-installed or core plugin.

  e.g. If you have a user-installed or core plugin that has a 'hello' command, installing a linked plugin with a 'hello'
  command will override the user-installed or core plugin implementation. This is useful for development work.


EXAMPLES
  $ jeep plugins link myplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.0.15/src/commands/plugins/link.ts)_

## `jeep plugins remove [PLUGIN]`

Removes a plugin from the CLI.

```
USAGE
  $ jeep plugins remove [PLUGIN...] [-h] [-v]

ARGUMENTS
  PLUGIN...  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ jeep plugins unlink
  $ jeep plugins remove

EXAMPLES
  $ jeep plugins remove myplugin
```

## `jeep plugins reset`

Remove all user-installed and linked plugins.

```
USAGE
  $ jeep plugins reset [--hard] [--reinstall]

FLAGS
  --hard       Delete node_modules and package manager related files in addition to uninstalling plugins.
  --reinstall  Reinstall all plugins after uninstalling.
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.0.15/src/commands/plugins/reset.ts)_

## `jeep plugins uninstall [PLUGIN]`

Removes a plugin from the CLI.

```
USAGE
  $ jeep plugins uninstall [PLUGIN...] [-h] [-v]

ARGUMENTS
  PLUGIN...  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ jeep plugins unlink
  $ jeep plugins remove

EXAMPLES
  $ jeep plugins uninstall myplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.0.15/src/commands/plugins/uninstall.ts)_

## `jeep plugins unlink [PLUGIN]`

Removes a plugin from the CLI.

```
USAGE
  $ jeep plugins unlink [PLUGIN...] [-h] [-v]

ARGUMENTS
  PLUGIN...  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ jeep plugins unlink
  $ jeep plugins remove

EXAMPLES
  $ jeep plugins unlink myplugin
```

## `jeep plugins update`

Update installed plugins.

```
USAGE
  $ jeep plugins update [-h] [-v]

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Update installed plugins.
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.0.15/src/commands/plugins/update.ts)_
<!-- commandsstop -->

## Contributors ✨

Thanks goes to these wonderful people ([emoji key](https://allcontributors.org/docs/en/emoji-key)):

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore-start -->
<!-- markdownlint-disable -->
<!-- markdownlint-restore -->
<!-- prettier-ignore-end -->
<!-- ALL-CONTRIBUTORS-LIST:END -->

This project follows the [all-contributors](https://github.com/all-contributors/all-contributors) specification. Contributions of any kind welcome!
