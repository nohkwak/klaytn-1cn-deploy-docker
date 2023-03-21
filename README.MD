# Deploying Klaytn local Network with 1CN

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

## Starting the Klaytn 
Execute the following script:

```bash
$ ./generateDockerCompose.sh
```

### Chainging parameters
You can change two parameters in `1.prepare.sh`.

| Parameter | Description |
|---|---|
|CHAIN_ID| The chain ID of the deployed chain. (Default:1000) |
|SCHAIN_ID| The service-chain ID of the deployed chain. (Default:2000) |
|NETWORK_ID| The network ID of the deployed chain. (Default:203) |
|NUM_CNS| Number of CNs of the network. (Default:1) |
|NUM_PNS| Number of PNs of the network. (Default:1) |
|NUM_ENS| Number of ENs of the network. (Default:1) |
|NUM_SCNS| Number of SCNs of the network. (Default:1) |

## Edit docker-compose file and execute the docker.
Update docker-compose.yml with <TagName> and account info. 

```bash
$ docker-compose up
```
