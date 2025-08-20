# 💻 Intellistor Frontend

Este repositório contém o **frontend da plataforma Intellistor**, uma solução inteligente para gestão de ambientes de armazenamento e backup corporativo. A interface foi projetada para oferecer uma experiência fluida, responsiva e integrada com o backend via APIs RESTful.

---

## 🧭 Visão Geral

O frontend da Intellistor permite:
- Visualizar e gerenciar ambientes de storage e backup
- Monitorar status e métricas operacionais
- Interagir com os módulos da plataforma de forma intuitiva
- Autenticar usuários e proteger rotas sensíveis

---

## 🛠️ Tecnologias Utilizadas

- **React.js** com Vite ou CRA *(dependendo do setup)*
- **TypeScript** *(opcional, mas recomendado)*
- **Axios** para consumo de APIs
- **React Router** para navegação
- **Tailwind CSS** ou **Styled Components** para estilização
- **Docker** para empacotamento e deploy

---

## 📦 Instalação

### 1. Clone o repositório
```bash
git clone https://github.com/seu-usuario/intellistor-frontend.git
cd intellistor-frontend
```

### 2. Instale as dependências
```bash
npm install
ou
yarn install
```

### 3. Configure as variáveis de ambiente
Crie um arquivo .env com a URL do backend:
```bash
VITE_API_URL=http://localhost:8000
```

### 4. Execute o projeto localmente
```bash
npm run dev
ou
yarn dev
```

### 5. A aplicação estará disponível em:
```bash
http://localhost:5173
````
---

## 🐳 Executar com Docker

### 1. Crie um Dockerfile com o seguinte conteúdo:
```bash
FROM node:18-alpine
WORKDIR /app
COPY . .
RUN npm install
RUN npm run build
EXPOSE 80
CMD ["npx", "serve", "dist"]
```

### 2. Crie um docker-compose.yml com o seguinte conteúdo:
```bash
version: '3.8'

services:
  frontend:
    build: .
    ports:
      - "3000:80"
    env_file:
      - .env
```

### 3. Execute com o seguinte comando: 
```bash
docker-compose up --build
```

---

## 🔗 Integração com o Backend

Certifique-se de que o backend esteja rodando e acessível na URL definida em VITE_API_URL. Exemplo de chamada com Axios:
```bash
axios.get(`${import.meta.env.VITE_API_URL}/storages`)
```

---

## 🧪 Testes: 
```bash
npm run test
```

---
## 📄 Licença

Este projeto está licenciado sob a MIT License – veja em [licença](#) 

---
## 🤝 Contribuições

Contribuições são bem-vindas! Sinta-se à vontade para abrir issues ou enviar pull requests.

---
## ✉️ Contato

Em caso de dúvidas, sugestões ou contribuições, entre em contato com os responsáveis pelo projeto:

- **Eloi Salton** — [e-mail](mailto:eloi.externo@petacorp.com.br)
- **Renato de Carvalho Machado** — [e-mail](mailto:renato.externo@petacorp.com.br)

---


