# README

Storage and storage related services for Ze

## About Ze Storage

The Ze project uses Neo4J, a native graph database that is built for the storage and retrieval of connected data (`graph` data). The devcontainer is built around the official Neo4J image. Neo4J provides a number of tools to reduce the friction of learning and developing with graph applications including the Neo4J browser.

## Neo4J Browser

The browser is useful for learning Cypher (the query language of Neo4J), and for visualizing and exploring data in the db. To access the browser, navigate to:

 `http://localhost:7474`

and enter the credentials.

## Credentials

Out of the box, the db credentials for the initial user are defined by default and you can learn more by reviewing the [Neo4J docs](https://neo4j.com/docs/operations-manual/current/configuration/set-initial-password/). If you wish to use a custom initial user password, you can define a `.env` file based on the existing `.env.example` and change the given password to your own. If you do not, the initial user credentials fallback defined in the `docker-compose.yaml` file will be used instead.

## Installation

Assuming you are running `DevPod` follow the steps below:

1) Fire up `DevPod`
2) Click `Workspaces` in left sidepane if it is not already selected
3) Click `Create Workspace`
4) Copy/paste repo url `https://github.com/leonardreidy/ze-data` to input under `Enter Workspace Source`
5) Choose default IDE (VSCode)
6) Enter a name for the workspace in the input under `Workspace Name`
7) Click `Create Workspace`

## Network

The network that the store shares with the other containers is defined in this repo. As such, if you bring up the others in advance, they will fail as the network doesn't yet exist. I will revisit this later. For now, it is adequate as it is simply a matter of spinning up this container first.

## IDE

If the chosen IDE is the browser variant of VSCode it should open automatically at:

`http://localhost:10800/?folder=/workspace`