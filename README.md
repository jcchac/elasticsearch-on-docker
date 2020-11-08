# Elasticsearch on Docker

> Source: https://www.elastic.co/guide/en/elastic-stack-get-started/current/get-started-docker.html

This repository contains a `docker-compose.yml` file to bring up a three-node Elasticsearch cluster and Kibana.

### Pre-requisites

- Install [Docker](https://docs.docker.com/get-docker/) and [Docker Compose](https://docs.docker.com/compose/install/)
- Make sure Docker Engine is allotted at least 4GiB of memory. In Docker Desktop, you can configure resource usage on the Advance tob in Preference (macOS) or Settings (Windows)

## Usage

1. Run `docker-compose` to bring up the three-node Elasticsearch cluster:

    ```sh
    $ docker-compose up
    ```

2. Submit a `_cat/nodes` request to see that the nodes are up and running:

    ```sh
    curl -X GET "localhost:9200/_cat/nodes?v&pretty"
    ```

3. Open Kibana to load sample data and interact with the cluster: http://localhost:5601

4. Tear down containers and volumens when you are done:

    ```sh
    $ docker-compose down -v
    ```
