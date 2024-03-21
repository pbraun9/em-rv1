# How to use an EM-RV1 as a Kosmos node

First you need a Kosmos cluster in version 1.29.1 and configured with an external node pool. You can follow [this guide](https://www.scaleway.com/en/docs/containers/kubernetes/how-to/create-kosmos-cluster/) to create your first Kosmos cluster.



Go on Scaleway [Elastic Metal console](https://console.scaleway.com/elastic-metal/servers/create?offerName=EM-RV1-C4M16S128-A&osId=1c376d8a-f237-438d-9cd9-47902050ffd3&pricing=monthly&zone=fr-par-2), select `fr-par-2` as region, order an EM-RV1 server under "Labs" section and select "Kosmos" as OS. Fill all information needed and don't forget your ssh keys.

1. Go on your Kosmos cluster in "Nodes" tab and click on "Add external node".
2. SSH into your EM-R1 server and start to follow instructions with the following modification: 
    - Ignore step 1, the binary is already setup on the server.
    - At step 3, run `sudo -E ./node-agent_linux_riscv64 -loglevel 0 -no-controller` instead of the suggested command.
3. **reboot** your server
