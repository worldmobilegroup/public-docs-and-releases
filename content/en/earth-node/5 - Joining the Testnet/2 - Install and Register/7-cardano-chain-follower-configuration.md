---
title: Cardano Chain Follower configuration
description: Setting the chain follower as a systemd service to run it on the same node.
weight: 7
---
The chain follower provides the information for AyA to stay consistent with the main chain. Here we will guide you on 
how to set up the chain follower as a systemd service and run it on the same node.

The Cardano Chain Follower (CCF) needs a working Cardano Node and DBSync connection. The standard read-only access to a
DBSync Node operated by World Mobile is already included in the default config, so you don't need to set up a DBSync on 
your own.

The DBSync is located in London, therefor, depending on the location of your EarthNode, you may experience a better or
worse connection. This may have an impact on the performance of your EarthNode. Of course, you can use your own DBSync 
if it suits you, the connection string is in the configuration file.

By default, all CCFs connect to the IOG preview node. We recommend that you choose another node (also in the CCF 
configuration file).

To configure the CCF, complete the following steps:
1. Download the latest CCF installation package.
2. Extract content to any directory.
3. Run the installation script `./install_ccf.sh`.
