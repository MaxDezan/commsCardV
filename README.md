# Formulário de Comissões de Arte — Skyartsies

Aplicação web interativa para exibição de catálogo de comissões artísticas, cálculo dinâmico de orçamento (incluindo cálculo de 50% para personagens extras) e envio de pedidos por e-mail.

Otimizada para deploy Serverless na **Vercel** ou execução local com **Node.js**.

---

## Tecnologias

- **Front-end**: HTML5, CSS3, JavaScript Vanilla
- **Back-end**: Node.js, Express (Serverless Functions na Vercel)
- **Serviço de E-mail**: Nodemailer (SMTP)

---

## Como Rodar Localmente

1. **Instale as dependências**:
   ```bash
   npm install
   ```

2. **Configure suas variáveis de ambiente**:
   Copie o arquivo `.env.example` para `.env`:
   ```bash
   cp .env.example .env
   ```
   Preencha suas credenciais de e-mail (Gmail App Password, etc.).

3. **Inicie o servidor**:
   ```bash
   npm start
   ```
   Acesse no navegador: **http://localhost:3000**

---

## Deploy na Vercel

1. Suba este projeto para um repositório no seu GitHub.
2. Acesse [vercel.com](https://vercel.com) e importe o repositório.
3. No painel de configuração do projeto na Vercel, adicione as **Environment Variables**:
   - `SMTP_HOST` (ex: `smtp.gmail.com`)
   - `SMTP_PORT` (ex: `587`)
   - `SMTP_USER` (seu e-mail)
   - `SMTP_PASS` (sua senha de aplicativo do e-mail)
   - `EMAIL_DESTINO` (e-mail onde você quer receber os pedidos)
4. Clique em **Deploy**! A Vercel vai gerar uma URL pública com HTTPS automático para o seu formulário.
