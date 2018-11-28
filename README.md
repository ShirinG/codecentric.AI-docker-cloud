# codecentricAI-docker
Dockerfile for codecentricAI Bootcamp environment

## Run from Dockerhub

### Jupyterlab starten
```bash
docker pull codecentric/from-keras-to-production-baseimage
```

### Run on Mac & Linux

```bash
docker run -p 8888:8888 -v $(pwd)/notebooks:/keras2production/notebooks codecentric/from-keras-to-production-baseimage
```

### Run on Windows

```bash
docker run -p 8888:8888 -v %cd%/notebooks:/keras2production/notebooks codecentric/from-keras-to-production-baseimage
```

## Build locally

```bash
git clone https://github.com/codecentric/codecentric.AI-docker.git
cd codecentric.AI-docker

docker build -t codecentric.ai-docker .

git clone https://github.com/codecentric/codecentric.AI-bootcamp
cd codecentric.AI-bootcamp

docker run -p 8888:8888 -v $(pwd)/notebooks:/notebooks codecentric.ai-docker
```
