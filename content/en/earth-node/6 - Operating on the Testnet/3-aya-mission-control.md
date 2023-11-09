---
title: AyA Mission Control (AMC)
description: The default monitoring system for your EarthNode.
weight: 3
---
AyA mission Control (AMC) is a monitoring and alerting dashboard for your EarthNode.

To use AMC, we must do the following:

## Update EarthNode Configuration
The API server must be enabled in configuration.

To update the default EarthNode configuration, complete the following steps:
1. Open a terminal
2. Check that the cosmovisor service is active using the following command:

    `sudo systemctl status cosmosvisor.service`

## Clone AMC Repository and Install
1. Clone the repository using the following command in your terminal:
    `git clone https://github.com/Sbcdn/aya-mission-control.git`
    {{<alert title="Note">}}For further information on cloning GitHub repositories, refer to the 
    [Cloning a repository](https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository) topic
    in the GitHub documentation.{{</alert>}}
2. The aya-mission-control directory is created.
3. Navigate to the AMC directory using the following command: `cd aya-mission-control`
4. Make the installation script runnable using the following command: `sudo chmod +x ./install_script.sh`
5. Run the installation script using the following command: `./install_script.sh`
    The installation script install AMC and some tools, such as Grafana.
6. Check that AMC installed successfully using the following command:
    `sudo systemctl status aya_mission_control.service`
    If successful, AMC is found and shown as active.

## Configure AMC
Before you can use AMC, you must configure it with the details of your EarthNode.

To configure AMC, you need the following information:
* Your validator address. This is also known as the account address, and starts with _aya_.
* The name of your EarthNode. This is also known as the moniker.
* Your validator hex address. This is also known as the account hex address.
* Your operator address. This is also known as the consensus address, and starts with _ayavalcons_

### Find the Account Address and EarthNode name
To find the account address and EarthNode name, complete the following steps:
1. In a terminal, navigate to the _/opt/aya_ directory, using the following command: `cd /opt/aya`
2. Display the content of the registration.json file using the following command: `cat registration.json`
    The name of your EarthNode, and your account and consensus addresses display.
    {{<alert title="Note">}}The account address starts with _aya_ and the consensus address starts with _ayavalcons_.{{</alert>}}
3. Copy this information and paste somewhere that you can access when editing the configuration.

### Find the Account Hex Address and Consensus Address
To find your account hex address and consensus address, complete the following steps:
1. Copy the account address entry and paste it in the proper place on the following command:
   `ayad keys parse <operator address>`
2. The bytes value (account hex address) of the account address displays.
3. Copy the byte address and paste somewhere that you can access when editing the configuration.
4. Paste the byte address in the proper place on the following command: `ayad keys parse <byte address>`
5. A list of addresses display. The consensus address is the third address in the list, and starts with _ayavaloper_.
6. Copy the consensus address and hex address.
7. Paste the consensus address and hex address somewhere that you can access when editing the configuration.

### Complete the configuration
To complete the configuration, complete the following steps:
1. Open the _/opt/aya/amc/config.toml_ file in your favourite text editor.
    
    For example, to open the file in the _nano_ command line text editor, enter the following command: `nano config.toml`.
2. Update the _val_operator_addr_ entry to match the consensus address. This is used to get your staking, delegation, 
and distribution rewards.
3. Update the _account_addr_ entry to match your account address. This is used to get information about your account.
4. Update the _validator_hex_addr_ entry to match your account hex address. This is used to get information about your
last proposed block, missing blocks and voting power.
5. Optionally, update the following entries:
    * _external_rpc_: This defines a secondary remote procedure call endpoint that can be used to ensure that the
   validator is up-to-date and check any synchronisation or missed blocks. You can use either of the following endpoints:
        * 34.67.7.216:26657
        * 34.121.228.97:26657
        * 34.163.11.82:26657
        * 34.163.200.162:26657
    * _enable_telegram_alerts_: By default, you won't receive telegram alerts. If you want to receive these alerts, set
   this entry to _yes_.
    * _enable_email_alerts_: By default, you won-t receive email alerts. If you want to receive these alerts, set this 
   entry to _yes_.
   {{<alert title="Note">}}For further instructions on the available configuration, refer to the INSTRUCTIONS.md file
    in the root of the tool's repository.{{</alert>}}
6. Update the _validator_name_ entry to match the name of your EarthNode
7. Save the file
8. Restart AMC to apply the updated configuration using the following command:
`sudo systemctl restart aya_mission_control.service`
9. Ensure that AMC has restarted successfully using the following command:
`sudo systemctl status aya_mission_control.service`
{{<alert title="Note">}}You might see an error about converting a string to int in the information. You can ignore this.{{</alert>}}
