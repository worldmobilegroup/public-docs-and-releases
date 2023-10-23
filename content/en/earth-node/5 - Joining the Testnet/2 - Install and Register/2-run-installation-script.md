---
title: Run the installation script
description: The installation script installs everything you need to run your EarthNode.
weight: 2
---
To install the EarthNode, complete the following steps:
1. Open a terminal.
2. Enter the following command in your terminal (from the directory where you unpacked the zip file)
    ```shell
    $ ./install_node.sh -m <name to use for the node> -a <name of the operator account>
    ```
    {{<alert title="Note">}}Syntax help displays if you enter `./install_node.sh`. The name of the node and the operator account are set as part of the installation to match the entered information and can be chosen by you. The operator account is stores locally only and is used to store keys in the keyring.{{</alert>}}
3. When prompted, enter a secure keyring passphrase.
{{<alert title="Note">}}The passphrase does not display on the screen.{{</alert>}}
4. When prompted, confirm the keyring passphrase by entering the same secure keyring passphrase again.
5. Store the mnemonic for account recovery, which is displayed after you have confirmed your keyring passphrase.
{{<alert title="Warning">}}This mnemonic provides the only way to recover your account. It is not displayed again.{{</alert>}}
6. Copy the JSON structure. You need this when registering your EarthNode, as described in the [Register the EarthNode topic.](/earth-node/5-joining-the-testnet/2-install-and-register/4-register-the-earthnode)

__Synchronisation of the EarthNode starts.__
{{<alert title="Note">}}The node will use `state-sync` mode to sync with chain. This means, that in place of syncing from block 1 (what can take, depending on the number of blocks that need to be synchronised and the speed of your
connection, up to several days or even weeks), it will use latest snapshot of network state that generates every 15000 blocks. In this case synchronisation should take few minutes at max.{{</alert>}}

Until synchronisation is complete, you cannot get a delegation. However, you can connect your wallet to World Mobile
and register your EarthNode with the ENNFT in your wallet, before synchronisation is complete.
{{<alert title="Note">}}If you register your EarthNode before installation is complete and the script fails,
you must re-run the script. Rerunning the script generates a new moniker for your EarthNode. If this happens, you
must deregister your EarthNode and register again using the updated JSON structure. For information on deregistering your
EarthNode, see the [Deregister the EarthNode topic](/earth-node/5-joining-the-testnet/2-install-and-register/5-deregister-the-earthnode){{</alert>}}
