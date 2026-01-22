# 🐳 Conceitos Fundamentais do Docker

## 1. Imagem Docker
🖼️ **O que é uma imagem?**

Uma imagem Docker é um **template imutável** que contém tudo o que é necessário para executar uma aplicação:

- Código da aplicação
- Bibliotecas
- Dependências
- Variáveis básicas
- Configurações

As imagens são utilizadas como base para criar containers.

📌 Exemplos:
- `nginx`
- `mysql`
- `redis`
- `ubuntu`

---

## 2. Container Docker
📦 **O que é um container?**

Um container é uma **instância em execução de uma imagem Docker**.

Características principais:
- Leve
- Isolado
- Rápido
- Efêmero (pode ser destruído e recriado facilmente)

📌 Relação importante:
> **Imagem é o modelo, container é a execução.**

---

## 3. Dockerfile
📄 **O que é um Dockerfile?**

O Dockerfile é um **arquivo de texto** que contém instruções para criar uma imagem Docker.

Ele define:
- Imagem base
- Dependências
- Comandos de build
- Porta exposta
- Comando de inicialização

📌 Exemplo simples:
```dockerfile
FROM nginx
COPY . /usr/share/nginx/html
