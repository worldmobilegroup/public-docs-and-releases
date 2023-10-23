---
title: Troubleshooting
description: If you experience any issues on AyA, the following solutions might help. 
weight: 2
---
## Unjail Validator
If your validator fails to commit blocks, for example due to a connection loss or server failure, it might be jailed.
Another reason your validator might be jailed is where two signed messages are submitted for the same block when validating
a private key.

Ensure that you monitor the performance of your node to allow any issues to be corrected before the validator is jailed.

When your validator is jailed, it cannot commit blocks until it has been unjailed. This process ensures the security and
performance of the network.

Your validator can be unjailed after the jail period elapses, and you can rejoin the network. This must be done manually
using the unjail transaction.

If your validator is jailed, you can unjail it using the following command:

```shell
$ ayad tx slashing unjail --from <yourAccountName> --home /opt/aya --chain-id <chainIdHere>
```
