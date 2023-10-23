---
title: Set collateral
description: Set a collateral to enable proper smart contract execution. 
weight: 4
---
## Set collateral
To interact with a smart contract, you must have the first address of the chain, and it
must have Unspent Transaction Outputs (UTxOs), and collateral.

UTxOs are the leftover cryptocurrency from your transactions, like the change you get
when buying something from the shop. At the moment, you might have a single UTxO, 
which is the test ADA you received when adding funds to your wallet.

To set collateral, complete the following steps:
1. In Eternl, select your wallet.
2. Select __Settings__ from the options at the top of the screen.
3. Select __Collateral__. The Collateral settings display.
4. Select the toggle to enable collateral.
5. Select the __Set Collateral__ button. 
6. Enter your password in the __Sign__ text box.
7. Select the __Sign__ button.

A transaction is made, where five ADA are sent from your wallet to yourself to be
used as collateral for smart contracts.

Now you can see two UTxOs, as follows:
* The funds in your wallet, which have been reduced by the collateral and the fee for
the transaction.
* The five ADA we have set as collateral.

## Refund the first address
When setting collateral, you sent funds from the first address in the chain 
(`'0'/0/0`) to a new address in the chain (`'0'/1/0`). This means that your first 
address is no longer funded. To resolve this, you will send funds to your first address.
{{<alert title="Note">}}You can find out which address is funded by selecting 
__Account__ from the top of the Eternl screen, then selecting the __UTxO List__ option.{{</alert>}}

To send funds to your first address, complete the following steps:
1. Select __Receive__ from the top of the screen and copy the first address.
2. Select __Send__ from the top of the screen.
3. Paste the first address in the __Receive Address__ text box.
4. Select the __Next__ button.
5. Enter _150_ in the __Funds__ text box.
6. Select the __Next__ button.
7. Enter your password in the __Sign__ text box.
8. Select the __Sign__ button.

The transaction is made, and your wallet is ready for use.
