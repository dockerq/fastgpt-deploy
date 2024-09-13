# FastGPT quick deploy

## install docker

refer [准备 Docker 环境](https://doc.fastgpt.in/docs/development/docker/#2-%e5%87%86%e5%a4%87-docker-%e7%8e%af%e5%a2%83)

## version info

version in current fastgpt

- fastgpt:v4.8.6
- oneapi:v0.6.7
- pgvector:0.7.0-pg15
- mongo:5.0.18
- mysql:8.0.36

## deploy

1. clone this repo
   ```shell
   git clone https://github.com/dockerq/fastgpt-deploy.git
   ```
2. pull image
   ```shell
   cd fastgpt-deploy
   docker compose pull
   ```
3. run image
   ```shell
   docker compose up -d
   ```

## config

[如何自定义配置文件？](https://doc.fastgpt.in/docs/development/docker/#%e5%a6%82%e4%bd%95%e8%87%aa%e5%ae%9a%e4%b9%89%e9%85%8d%e7%bd%ae%e6%96%87%e4%bb%b6)

1. change config in `config.json`
2. remove fastgpt
   ```shell
   docker compose down fastgpt
   ```
3. rerun fastgpt
   ```shell
   docker compose up -d fastgpt
   ```

## ollama endpoint

1. if you run in Linux, endpoint is `http://172.17.0.1:11434`
2. if you run in MacOS, endpoint is `http://host.docker.internal:11434`
