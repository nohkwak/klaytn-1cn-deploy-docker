# Deploying Klaytn 1CN with Docker

## Prerequisites
Following packages are required.

1. [Docker](https://docs.docker.com/get-docker/)
2. [Docker-compose](https://docs.docker.com/compose/install/)
3. [Klaytn](https://github.com/klaytn/klaytn)

## Make the new version of Klaytn 
To check out the local Klaytn network is working well, first check the status of the docker containers. To do that, execute the following command:

```bash
$ cd  'klaytn repository folder'
$ docker  build  -t  <TagName>  . 
```

## Generate docker-compose file
Execute the following script:

```bash
$ ./generateDockerCompose.sh
```

### Changing parameters
You can change the following parameters in `generateDockerCompose.sh`.

| Parameter | Description |
|---|---|
|CHAIN_ID| The chain ID of the deployed chain. (Default:1000) |
|SCHAIN_ID| The service-chain ID of the deployed chain. (Default:2000) |
|NETWORK_ID| The network ID of the deployed chain. (Default:203) |
|NUM_CNS| Number of CNs of the network. (Default:1) |
|NUM_PNS| Number of PNs of the network. (Default:0) |
|NUM_ENS| Number of ENs of the network. (Default:0) |
|NUM_SCNS| Number of SCNs of the network. (Default:0) |

## Edit docker-compose file and execute the docker.
Update `<TagName>` of the docker image and account info in `docker-compose.yml`.

```bash
$ docker-compose up
```
