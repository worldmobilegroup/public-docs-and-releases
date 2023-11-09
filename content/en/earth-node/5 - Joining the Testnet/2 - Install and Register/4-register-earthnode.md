---
title: Register EarthNode and Become a Validator
description: Use the EarthNode Registration Manager to register your EarthNode.
weight: 4
---
To register the EarthNode in the EarthNode Registration Manager, complete the following steps:
1. Select the __EarthNode Registration__ tab at the top of the Registration Manager.
2. Ensure that the wallet is connected and the ENNFT is selected; to ensure that the wallet is synchronised, select the
__Update Wallet Data__ button.
3. If necessary, select __RegisterEarthNode__ from the __Select Transaction Type__ drop-down menu.
4. Paste the JSON structure that you copied when running the installation script in the __Paste Installation Script
Output__ text box.
5. Select the __Build Transaction__ button. The Eternl transaction window displays.
6. Enter your Eternl password in the __Sign__ text box.
7. Select the __Sign__ button. When the transaction completes, a message displays in the EarthNode Registration Manager.
If successful, the transaction hash is included in the success message. If you select the transaction hash, you can view
the details of the transaction in a Cardano explorer, for example [Cexplorer](https://preview.cexplorer.io/tx/6588923dcc6968ce51b889b9ac14fd5be578ce276c94185e412dabcd8618baf4).

You can now return to the terminal and check on the synchronisation of your EarthNode.

When the synchronisation completes, the script will wait until information from the Cardano transaction reaches AyA (usually take 20-25 minutes).

Congratulations, you are now a validator.

{{<alert title="Note">}}If you register your EarthNode before installation is complete and the script fails, you must
re-run the installation script as described in the
[Run the Installation Script](/earth-node/5-joining-the-testnet/2-install-and-register/2-run-installation-script) topic. Rerunning
the script generates a new JSON structure for your EarthNode. If this happens, you must deregister your EarthNode and register
again using the updated data. For information on deregistering your EarthNode, see the 
[Deregister the EarthNode](/earth-node/5-joining-the-testnet/2-install-and-register/5-deregister-the-earthnode) topic.{{</alert>}}
