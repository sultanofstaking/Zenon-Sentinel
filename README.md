# Zenon-Sentinel-Deployment

## WARNING: I created this guide as an experiment for those setting up a sentinel on alphanet. The steps below are my own and not endorsed by the Zenon team. This is being done in a very agile way, MVP of an experiment I expect our cross-functional community will participate and provide feedback so we can continuously improve. Please use the issue feature for fixes here. If you need to reach me 1:1 DM me on TG @SultanOfStaking - Try at your own risk. 

## Sentinel Node requirements

Hardware, CPU >= 4 cores, RAM >= 4 GB, Storage >= 40 GB free space, >100Mbps network dedicated bandwidth
Software, Linux distros e.g. Ubuntu 20.04 LTS/Debian 11 (recommend ubuntu 20.04)

Also Recommended NTP configuration*, Recommended Watchdog service* **These are Included if the setup is performed using the znn-controller**

You will need 5k tZNN and 50k tQSR in the syrius address you are using to spawn your sentinel. 

## A few notes before you start...
1. Treat technical, security, and wallet address strategy like it will carry over into alphanet
2. Install the bundle from root as default data paths are set up that way
3. Ensure any address you are interacting with in syrius has plasma fused otherwise you risk needing to wait for plasma to be generated.

## Sentinel Install (fresh install on new VPS)
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

Enable RPC

`./znn-cli enableRPC`

Start znnd

`./znn-cli start znnd`

# Deploy Pillar or Sentinel

`./znn-controller`

Select ? to deploy the sentinel.


To diagnose errors or pull logs go here https://github.com/sultanofstaking/Zenon-Testnet-Node-Tips

## If you found helpful no need to donate, but delegation to SultanOfStaking pillar would be appreciated https://explorer.znn.space/pillar/z1qpgdtn89u9365jr7ltdxu29fy52pnzwe4fl7zc 
