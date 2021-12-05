# Zenon-Sentinel-Deployment

## WARNING: I created this guide as an experiment for those setting up a sentinel on alphanet. The steps below are my own and not endorsed by the Zenon team. This is being done in a very agile way, MVP of an experiment I expect our cross-functional community will participate and provide feedback so we can continuously improve. Please use the issue feature for fixes here. If you need to reach me 1:1 DM me on TG @SultanOfStaking - Try at your own risk. 

## Sentinel Node stated requirements

Hardware, CPU >= 4 cores, RAM >= 4 GB, Storage >= 40 GB free space, >100Mbps network dedicated bandwidth
Software, Linux distros e.g. Ubuntu 20.04 LTS/Debian 11 (recommend ubuntu 20.04)

Also Recommended NTP configuration*, Recommended Watchdog service* **These are Included if the setup is performed using the znn-controller**

## A few notes before you start...
1. The requirements above are minimum requirements provided by the team. **Nodes must have a daily uptime of over 90% to be eligible for rewards.** Block 27070 hung many nodes running at the minimum requirements without swap space. Because of this I would recommend you opt for a machine with at least 8GB ram and set up swap space. If you need help with your VPS set-up you can refer to my tips guide here https://github.com/sultanofstaking/VPS-Set-Up-Tips
2. You will need 5k ZNN and 50k QSR in the syrius address you are using to spawn your sentinel. These funds are locked for 27 days. At the end of the 27 days a 3 day windos opens to revoke the node and unlock your ZNN and QSR. This cycle repeats until your node is revoked.
3. Ensure any address you are interacting with in syrius has plasma fused otherwise you risk needing to wait for plasma to be generated.
4. **As of Decmenber 5th 2021 the team has not updated znn-controller to run sentinels on a VPS. You can register a sentinel in syrius through the sentinel tab by following the prompts. Once registered the 27 day cooldown begins. You should see rewards after 1 full day of activity i.e., the node needs to have an uptime of over 90% for 1 full epoch before you will be able to claim rewards in syrius. You will need to revisit this guide once the team provides steps to link your sentinel to a virtual machine.**

## Deploy Sentinel on a new VPS
**THE STEPS BELOW ARE FOR DOWNLOADING THE BUNDLE ONLY AND ARE NOT NEEDED AT THIS TIME TO RUN A SENTINEL. THIS SECTION WILL BE UPDATED ONCE THE TEAM UPDATES ZNN-CONTROLLER**

Start from root - if you are not sure enter the line below

`sudo su - root`

Install prereqs

`sudo apt install unzip`

`sudo apt install wget`

`sudo apt install gnupg`

Download bundle

`cd ~ && wget https://github.com/zenon-network/znn-bundle/releases/download/v0.0.1-alphanet/znn-alphanet-bundle-linux-amd64.zip`

Check testnet Quickstart https://testnet.znn.space/#!quickstart.md on how to verify bundle

Extract package

`unzip znn-alphanet-bundle-linux-amd64.zip`

Ensure all was extracted ok

`ls -lah`

You should see znn-cli, znnd, znn-controller, and corresponding argon2 and powlinks libraries

# Deploy Sentinel
**THIS SECTION WILL BE UPDATED ONCE THE TEAM UPDATES ZNN-CONTROLLER**

To diagnose errors in your sentinel or to learn how to pull logs go here https://github.com/sultanofstaking/Zenon-Testnet-Node-Tips

## If you found helpful no need to donate, but delegation to SultanOfStaking pillar would be appreciated.
