# 📄 — Comandos Básicos do Docker

---

## 🐳 Verificando o Docker

```bash
docker --version
```

Verifica se o Docker está instalado e mostra a versão.

```bash
docker info
```

Exibe informações do ambiente Docker (storage, driver, containers, imagens etc).

---

## 📦 Comandos de Imagens

### Listar imagens

```bash
docker images
```

### Baixar uma imagem do Docker Hub

```bash
docker pull nginx
```

### Remover imagem

```bash
docker rmi <image_id>
```

### Buildar imagem a partir do Dockerfile

```bash
docker build -t minha-imagem:1.0 .
```

---

## ▶️ Comandos de Containers

### Rodar um container

```bash
docker run nginx
```

### Rodar em background e mapear portas

```bash
docker run -d -p 8080:80 --name nginx-test nginx
```

### Listar containers em execução

```bash
docker ps
```

### Listar todos os containers

```bash
docker ps -a
```

### Parar um container

```bash
docker stop nginx-test
```

### Inspecionar um container

```bash
docker inspect nginx-test
```

### Iniciar container parado

```bash
docker start nginx-test
```

### Remover container

```bash
docker rm nginx-test
```

---

## 🧪 Logs e Debug

### Ver logs do container

```bash
docker logs nginx-test
```

### Acessar o container 

```bash
docker exec -it nginx-test bash
```

---

## 🗂️ Volumes e Persistência

### Criar volume

```bash
docker volume create meu-volume
```

### Listar volumes

```bash
docker volume ls
```

### Usar volume no container

```bash
docker run -d -v meu-volume:/dados nginx
```

---

---

## 🧹 Limpeza (muito importante)

### Remover containers parados

```bash
docker container prune
```

### Remover imagens não utilizadas

```bash
docker image prune
```

### Limpeza geral

```bash
docker system prune
```
