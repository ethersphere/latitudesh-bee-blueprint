# Latitude.sh Blueprint for Swarm Bee Light Node 
Latitude.sh Launchpad blueprint to run a [Swarm](https://docs.ethswarm.org/) Bee [light node](https://docs.ethswarm.org/docs/bee/working-with-bee/light-nodes). This blueprint also installs [Swarm-CLI](https://github.com/ethersphere/swarm-cli) for interacting with the bee node.

## About Swarm
Swarm is a peer-to-peer network of Bee nodes that collectively provide censorship resistant decentralised storage and communication services. Swarm's mission is to shape the future towards a self-sovereign global society and permissionless open markets by providing scalable base-layer data storage infrastructure for the decentralised internet. Its incentive system is enforced through smart contracts on the Gnosis Chain blockchain and powered by the xBZZ token, making it economically self-sustaining.

## Using the blueprint on Latitude.sh

### Environment Variables on Latitude.sh

Each of the following environment variable is optional, set either `SSH_PASSWORD` or `PUBLIC_KEY` for ssh access

| Variable     | Description                             |
| ------------ | --------------------------------------- |
| PUBLIC_KEY   | Public Key for ssh access               |
| SSH_USER     | Username for ssh access (default: root) |

### SSH access on Latitude.sh

To enable SSH access, enter your public SSH key in the `PUBLIC_KEY` environment variable during deployment. After deployment, use the provided IP address and the following command to connect:

```
ssh root@<APP_IP> -p 22
```

## Getting started after deploying Swarm Lightnode
Connect to your instance with `ssh root@<APP_IP> -p 22`

Verify Bee node status with `swarm-cli status`

### Participate in the Swarm network: 
- Documentation - https://docs.ethswarm.org/
- Discord - https://discord.ethswarm.org/
- Bee - https://github.com/ethersphere/bee
- Swarm-CLI - https://github.com/ethersphere/swarm-cli

## Development

### Running the docker image
```bash
docker pull ethersphere/latitudesh-bee-blueprint:latest
docker run -d -p 1633:1633 ethersphere/latitudesh-bee-blueprint:latest
```

### Building the docker image locally
```bash
git clone https://github.com/ethersphere/latitudesh-bee-blueprint.git
cd latitudesh-bee-blueprint
docker build -t ethersphere/latitudesh-bee-blueprint:latest
```

