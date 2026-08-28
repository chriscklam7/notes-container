# Notes of Container

## Docker

### Docker compose

<details>
<summary>Check container</summary>

```shell
docker compose ps
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
docker compose restart [CONTAINER_NAME]
```

</details>

<details>
<summary>Get into running container's bash</summary>

```shell
docker exec -it [CONTAINER_NAME] bash
```

</details>

<details>
<summary>Get into stopped container's bash</summary>

```shell
docker compose run --rm [CONTAINER_NAME] bash
```

</details>

<br />

## Kubernetes
