# Notes of Container

## Docker

### Basic

<details>
<summary>List running container</summary>

```shell
docker ps
```

</details>

<details>
<summary>List all containers</summary>

```shell
docker ps -a
```

</details>

<details>
<summary>List image</summary>

```shell
docker images
```

</details>

<details>
<summary>Remove container</summary>

```shell
docker rm [CONTAINER_ID]
```

</details>

<details>
<summary>Remove all running containers</summary>

```shell
docker container prune -f
```

</details>

<details>
<summary>Remove all containers</summary>

```shell
docker rm -f $(docker ps -aq)
```

</details>

<details>
<summary>Remove image</summary>

```shell
docker rmi [CONTAINER_ID]
```

</details>

<details>
<summary>Remove all images</summary>

```shell
docker rmi -f $(docker images -aq)
```

</details>

<details>
<summary>Remove all images and caches</summary>

```shell
docker image prune -a -f
```

</details>

### Compose

<details>
<summary>List container</summary>

```shell
docker compose ps
```

</details>

<details>
<summary>Build</summary>

```shell
docker compose build
```

</details>

<details>
<summary>Build and up all containers</summary>

```shell
docker compose up --build
```

</details>

<details>
<summary>Build and up all containers in the background</summary>

```shell
docker compose up --build -d
```

</details>

<details>
<summary>Down all containers</summary>

```shell
docker compose down
```

</details>

<details>
<summary>Clean cache and rebuild all containers</summary>

```shell
docker compose build --no-cache
docker compose up -d
```

</details>

<details>
<summary>Restart all containers</summary>

```shell
docker compose restart
```

</details>

<details>
<summary>Restart 1 container</summary>

```shell
docker compose restart [CONTAINER_ID]
```

</details>

<details>
<summary>Get into running container's bash</summary>

```shell
docker exec -it [CONTAINER_ID] bash
```

</details>

<details>
<summary>Get into stopped container's bash</summary>

```shell
docker compose run --rm [CONTAINER_ID] bash
```

</details>

<details>
<summary>Run the Docker app with a local folder mounted when the app starts</summary>

```shell
docker compose run --rm -v "/local-folder:/input" [DOCKER_APP] [COMMAND_IN_DOCKER]
```

</details>

<details>
<summary>Run docker app ignoring "Creating" | "Created" when the app starts</summary>

```shell
docker compose run --rm [DOCKER_APP] [COMMAND_IN_DOCKER] > >(grep -v '\[WARNING\]') 2> >(grep -Ev 'Container .* (Creating|Created)|\[WARNING\]' >&2)
```

</details>

<br />

  
## Kubernetes
