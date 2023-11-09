---
title: Ayad CLI quick reference
description: Reference of the different commands that the ayad CLI binary offers.
weight: 1
---

World Mobile provides a command line interface (CLI) tool, named `ayad`.

## Command format

The tools can be used by following this format:
`ayad [command]`

Valid commands and their arguments are described in the CLI Tool Commands section below.

You can view the Command Line Help as described in the CLI tool Help section below.

## Commands

The commands provided by the `ayad` CLI tool are described below:

| Commnad               | Description                                                                                               |
|-----------------------|-----------------------------------------------------------------------------------------------------------|
| `add-genesis-account` | Add the specified account to the genesis.json file.                                                       |
| `collect-gentxs`      | Collect genesis transactions and output a genesis.json file.                                              |
| `config`              | Create or query an application CLI configuration file.                                                    |
| `debug`               | Tool for helping with debugging your application.                                                         |
| `export`              | Export the specified state to JSON.                                                                       |
| `gentx`               | Generate a genesis transaction that carries self-delegation.                                              |
| `help`                | Display help on the specified command.                                                                    |
| `init`                | Initialise the private validator, p2p, genesis, and application configuration files.                      |
| `keys`                | Manage application keys.                                                                                  |
| `migrate`             | Migrate genesis to the specified target version.                                                          |
| `query`               | Query the specified subcommand.                                                                           |
| `rollback`            | Rollback the cosmos-sdk and tendermint stat by one height.                                                |
| `start`               | Run the EarthNode.                                                                                        |
| `tendermint`          | Run the specified tendermint subcommand.                                                                  |
| `tx`                  | Run the specified transaction subcommand.                                                                 |
| `validate-genesis`    | Validate the genesis file at the default location, or if supplied as an argument, the specified location. |
| `version`             | Display the binary version.                                                                               |

The flags used by the `ayad` CLI tool are described below:

| Flag                  | Description                                                                                                                               |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `--help` or `-h`      | Display help for the specified command                                                                                                    |
| `--home string`       | Define the directory for configuration and data. By default, this is `/home/ubuntu/.aya`.                                                 |
| `--log_format string` | Define the format used for the log file. Valid values are `json` or `plain`. By default, this is set to `plain`.                          |
| `--log_level string`  | Set the loggin level. Valid values are `trace`, `debug`, `info`, `warn`, `error`, `fatal`, or `panic`. By default, this is set to `info`. |
| `--trace`             | Print the full stack trace for errors.                                                                                                    |

## CLI Tool Help

You can access help for the `ayad` CLI at any time using the following command:
`ayad -h`

To display help for any command, use the following format:
`ayad [command] --help`
