---
title: Unzip the package
description: Unzip the package containing the installation script and other required files.
weight: 1
---
The package contains the installation script, the command line interface tool, the
process manager, and other required files.

To unzip the EarthNode, complete the following steps:
1. Copy the provided AyA package to your machine.
2. Open a terminal.
3. Navigate to the directory to which you copied ZIP file.
4. If using a virtual machine (VM), upload the ZIP file to the VM.
{{<alert title="Note">}}For information on setting up and using a VM, including how
to find the IP address, see the documentation for the product you are using.{{</alert>}}
5. Unzip the download EarthNode testnet package file using the unzip command in
following format:
   ```shell
   $ unzip [downloaded zip file].zip -d [destination directory]
   ```
6. Navigate to the destination folder and check that the following files are listed
using the `ls` command:
    * `ayad`: This is the AyA command line interface (CLI). For further information
   on the CLI, see the [`ayad` CLI Quick Reference page](/earth-node/6-operating-on-the-testnet/1-ayad-cli-quick-reference).
    * `cosmovisor`: This is provided by the Cosmos team, and allows your node to perform
   automatic operations such as upgrades.
    * `genesis.json`: This is a configuration file that is used during the installation of your EarthNode.
    * `install.node.sh`: This is the installation script.
    * `release_checksums`: This is used to check and ensure the completeness and correctness of files and data.
