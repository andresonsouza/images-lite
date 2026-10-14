# 📷 ImagesLite - API & Aplicação Fullstack

![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.x-6DB33F?style=for-the-badge&logo=springboot&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)

Aplicação desenvolvida com o objetivo de gerenciar e armazenar imagens, manipulando metadados e tags. O projeto faz parte dos meus estudos na stack Java/Spring Boot e React, com base no curso *Spring Boot + ReactJS: Fullstack do Zero ao Deploy no Docker*, ministrado pelo instrutor Dougllas Sousa.

---

## 📌 Sobre o Projeto

O **ImagesLite** é uma solução para envio, categorização e busca de arquivos de imagem. O backend oferece endpoints RESTful para manipulação de dados e arquivos `multipart/form-data`, integrando-se a um banco de dados PostgreSQL e empacotado via containers Docker.

### Principais Funcionalidades

- **Upload de Imagens:** Envio de arquivos de imagem via requisições `multipart/form-data`.
- **Categorização:** Associação de metadados como nome e múltiplas `tags` para filtro.
- **Persistência de Dados:** Mapeamento de entidades e armazenamento relacional.
- **Conteinerização:** Ambiente configurado com Docker Compose para subir banco de dados e aplicação rapidamente.

---

## 🛠️ Tecnologias Utilizadas

### **Backend**
- **Java 17+**
- **Spring Boot 3** (Spring Web, Spring Data JPA)
- **PostgreSQL**
- **Maven**

### **Frontend**
- **React.js**
- **Tailwind CSS** (para estilização rápida e responsiva)

### **DevOps & Ferramentas**
- **Docker & Docker Compose**
- **Bruno / Postman** (para testes e documentação dos endpoints de API)

---

## 🚀 Como Executar o Projeto

### **Pré-requisitos**
- [JDK 17+](https://www.oracle.com/java/technologies/downloads/)
- [Node.js](https://nodejs.org/)
- [Docker](https://www.docker.com/) e Docker Compose

### **1. Clonar o repositório**
```bash
git clone https://github.com/andresonsouza/spring-boot-reactjs.git
cd imageslite
```

### **2. Executar o Banco de Dados com Docker**
```bash
docker-compose up -d
```

### **3. Executar o Backend (Spring Boot)**
```bash
cd backend
./mvnw spring-boot:run
```
> A API estará acessível em `http://localhost:8080`

### **4. Executar o Frontend (React)**
```bash
cd frontend
npm install
npm run dev
```

---

## 📬 Endpoints da API

| Método | Endpoint | Descrição | Content-Type |
| :--- | :--- | :--- | :--- |
| `POST` | `/v1/images` | Envia uma nova imagem com nome e tags | `multipart/form-data` |
| `GET` | `/v1/images` | Lista/busca imagens cadastradas | `application/json` |

---
