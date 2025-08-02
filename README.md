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

```bash
1. Clone o repositório
git clone https://github.com/seu-usuario/intellistor-frontend.git
cd intellistor-frontend

2. Instale as dependências
npm install
# ou
yarn install

3. Configure as variáveis de ambiente
Crie um arquivo .env com a URL do backend:
VITE_API_URL=http://localhost:8000

4. Execute o projeto localmente
npm run dev
# ou
yarn dev

5. A aplicação estará disponível em:
http://localhost:5173
````

---

## 🐳 Executar com Docker

### - Crie um Dockerfile com o seguinte conteúdo:

FROM node:18-alpine
WORKDIR /app
COPY . .
RUN npm install
RUN npm run build
EXPOSE 80
CMD ["npx", "serve", "dist"]

### - Crie um docker-compose.yml com o seguinte conteúdo:
version: '3.8'

services:
  frontend:
    build: .
    ports:
      - "3000:80"
    env_file:
      - .env

### - Execute com o seguinte comando: 

docker-compose up --build

---

## 🔗 Integração com o Backend

Certifique-se de que o backend esteja rodando e acessível na URL definida em VITE_API_URL. Exemplo de chamada com Axios:

axios.get(`${import.meta.env.VITE_API_URL}/storages`)

---

## 🧪 Testes: 
npm run test

---
## 📄 Licença

Este projeto está licenciado sob a MIT License – veja em [licença](#) 

---
## 🤝 Contribuições

Contribuições são bem-vindas! Sinta-se à vontade para abrir issues ou enviar pull requests.

---
## 📬 Contato

Para dúvidas, sugestões ou parcerias, entre em contato:
- Renato – renato@email.com (substitua pelo seu e-mail)
- [Linkedin](https://www.linkedin.com/in/renatodicmachado/)



