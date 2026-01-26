# 🐳 Docker Labs – Guia Completo

## 1. Pré-requisitos
📋 Antes de instalar o Docker, verifique se o ambiente atende aos requisitos básicos:

- Sistema operacional Linux, macOS ou Windows
- Acesso administrativo (root ou sudo)
- Conexão com a internet
- Kernel Linux atualizado (no caso de Linux)

> 💡 O Docker funciona melhor em sistemas Linux, pois utiliza diretamente recursos do kernel.

---

### 📌 Cenário utilizado
Neste laboratório, estou utilizando o **Ubuntu Linux** como sistema operacional.

---

## 2. Instalação do Docker no Linux
🐧 Exemplo para distribuições baseadas em **Debian / Ubuntu**

### 2.1 Atualizar o sistema
```bash
sudo apt update && sudo apt upgrade -y
```
### 2.2 Instalar dependências necessárias
```bash
sudo apt install -y ca-certificates curl gnupg
```

### 2.3 Adicionar a chave GPG oficial do Docker e o repositório
```bash
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```
### 2.4 Instalar o Docker Engine
```bash
sudo apt update && sudo apt install -y docker-ce docker-ce-cli containerd.io
```

### 3 **Adicionar o usuário ao grupo docker**
```bash
sudo usermod -aG docker $USER
```


### 4.1 Instalação do Docker Compose
```bash
sudo curl -L "https://github.com/docker/compose/releases/download/$(curl -s https://api.github.com/repos/docker/compose/releases/latest | grep 'tag_name' | cut -d '\"' -f4)/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
```

### 4.2 Ajustar permissões de execução
```bash
sudo chmod +x /usr/local/bin/docker-compose
```

### 4.3 Verificar instalação
```bash
docker-compose --version
```

### 5. Verificação da instalação do Docker
```bash
docker-compose --version
```















