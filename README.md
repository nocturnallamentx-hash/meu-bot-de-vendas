# meu-bot-de-vendas
Norvl | Vendas: Transforme seu Discord em uma loja completa! Gerencie produtos, receba pagamentos via Mercado Pago (PIX/Cartão) com entrega automática, crie cupons, ofereça suporte via tickets e automatize boas-vindas. Tudo em um painel web intuitivo. Sua solução definitiva para vendas no Discord!


# 🤖 Bot de Vendas Discord

Um bot completo de vendas para Discord com integração ao Mercado Pago, sistema de produtos, cupons, tickets de suporte e muito mais.

## ✨ Funcionalidades

### 🛒 Sistema de Vendas
- Loja de produtos integrada ao Discord
- Pagamentos automáticos via Mercado Pago
- Suporte a PIX e outros métodos de pagamento
- Entrega automática de produtos digitais
- Controle de estoque em tempo real

### 🎫 Sistema de Cupons
- Cupons de desconto por porcentagem ou valor fixo
- Controle de uso e expiração
- Aplicação automática durante a compra

### 🎫 Sistema de Tickets
- Suporte categorizado (Vendas, Técnico, Geral)
- Criação automática de canais privados
- Gerenciamento completo de tickets

### 👋 Sistema de Boas-vindas
- Mensagens automáticas para novos membros
- Sistema de verificação integrado
- Mensagens personalizáveis

### 📊 Painel Administrativo
- Interface web para gerenciamento
- Estatísticas em tempo real
- Controle completo de produtos e vendas

## 🚀 Instalação

### Pré-requisitos
- Node.js 16.0.0 ou superior
- Conta no Discord Developer Portal
- Conta no Mercado Pago (para pagamentos)

### 1. Configuração do Bot Discord

1. Acesse o [Discord Developer Portal](https://discord.com/developers/applications)
2. Crie uma nova aplicação
3. Vá para a seção "Bot" e crie um bot
4. Copie o token do bot
5. Em "OAuth2 > URL Generator":
   - Selecione "bot" e "applications.commands"
   - Selecione as permissões necessárias
   - Use a URL gerada para adicionar o bot ao seu servidor

### 2. Configuração do Mercado Pago

1. Acesse o [Mercado Pago Developers](https://www.mercadopago.com.br/developers)
2. Crie uma aplicação
3. Copie o Access Token e Public Key

### 3. Instalação do Bot

1. Extraia o arquivo ZIP
2. Abra o terminal na pasta do projeto
3. Instale as dependências:
```bash
npm install
```

4. Configure o arquivo `.env`:
```bash
cp .env.example .env
```

5. Edite o arquivo `.env` com suas credenciais:
```env
# Discord Bot Configuration
DISCORD_TOKEN=seu_token_do_discord
CLIENT_ID=id_do_cliente_discord
GUILD_ID=id_do_seu_servidor

# Mercado Pago Configuration
MERCADO_PAGO_ACCESS_TOKEN=seu_access_token
MERCADO_PAGO_PUBLIC_KEY=sua_public_key

# Bot Configuration
PREFIX=!
ADMIN_ROLE_ID=id_do_cargo_admin
SUPPORT_CATEGORY_ID=id_da_categoria_suporte
WELCOME_CHANNEL_ID=id_do_canal_boas_vindas
LOGS_CHANNEL_ID=id_do_canal_logs
```

6. Inicie o bot:
```bash
npm start
```

## 📋 Comandos Disponíveis

### 🛒 Comandos de Loja
- `/loja` - Exibe a loja de produtos
- `/produto criar` - Criar novo produto (Admin)
- `/produto listar` - Listar produtos (Admin)
- `/produto editar` - Editar produto (Admin)
- `/produto deletar` - Deletar produto (Admin)

### 💰 Comandos de Vendas
- `/vendas listar` - Listar vendas (Admin)
- `/vendas aprovar` - Aprovar venda manualmente (Admin)
- `/vendas rejeitar` - Rejeitar venda (Admin)
- `/vendas status` - Verificar status de pagamento (Admin)

### 🎫 Comandos de Cupons
- `/cupom criar` - Criar cupom (Admin)
- `/cupom listar` - Listar cupons (Admin)
- `/cupom info` - Informações do cupom (Admin)
- `/cupom ativar/desativar` - Gerenciar status (Admin)

### 🎫 Comandos de Suporte
- `/suporte painel` - Criar painel de suporte
- `/suporte tickets` - Listar tickets (Admin)
- `/suporte fechar` - Fechar ticket (Admin)

### 👋 Comandos de Boas-vindas
- `/boasvindas testar` - Testar mensagem (Admin)
- `/boasvindas canal` - Configurar canal (Admin)
- `/verificacao painel` - Criar painel de verificação (Admin)

### ⚙️ Comandos de Configuração
- `/config info` - Informações de configuração (Admin)
- `/config stats` - Estatísticas do bot (Admin)

## 🌐 Painel Administrativo

Acesse `http://localhost:3000` para usar o painel web administrativo.

### Funcionalidades do Painel:
- Visualizar estatísticas em tempo real
- Gerenciar produtos
- Acompanhar vendas
- Criar e gerenciar cupons
- Configurações do sistema

## 🔧 Configuração Avançada

### Webhooks do Mercado Pago

Para receber notificações automáticas de pagamento, configure o webhook:

1. No painel do Mercado Pago, vá em "Webhooks"
2. Adicione a URL: `https://seu-dominio.com/webhook/mercadopago`
3. Selecione os eventos de pagamento

### Permissões do Bot

O bot precisa das seguintes permissões:
- Ler mensagens
- Enviar mensagens
- Gerenciar canais
- Gerenciar cargos
- Usar comandos slash
- Enviar mensagens privadas

### Estrutura de Canais Recomendada

```
📋 INFORMAÇÕES
├── 📜 regras
├── 📢 anúncios
└── 👋 boas-vindas

🛒 LOJA
├── 🛍️ produtos
└── 💳 pagamentos

🎫 SUPORTE
├── 📞 criar-ticket
├── 🔧 suporte-técnico
└── 💰 suporte-vendas

👥 GERAL
├── 💬 chat-geral
└── 🎮 comandos-bot
```

## 🐛 Solução de Problemas

### Bot não responde aos comandos
1. Verifique se o token está correto
2. Confirme se o bot tem permissões necessárias
3. Verifique se os comandos foram registrados

### Pagamentos não funcionam
1. Verifique as credenciais do Mercado Pago
2. Confirme se o webhook está configurado
3. Verifique os logs do console

### Tickets não são criados
1. Verifique se a categoria de suporte existe
2. Confirme as permissões do bot
3. Verifique o ID da categoria no .env

## 📝 Logs

O bot gera logs detalhados no console. Para debug:

```bash
# Modo desenvolvimento com auto-reload
npm run dev
```

## 🔒 Segurança

- Nunca compartilhe seu arquivo `.env`
- Use tokens de teste durante desenvolvimento
- Configure webhooks apenas em HTTPS
- Mantenha as dependências atualizadas

## 📞 Suporte

Para suporte técnico:
1. Verifique a documentação
2. Consulte os logs de erro
3. Verifique as configurações

## 📄 Licença

Este projeto está sob a licença MIT. Veja o arquivo LICENSE para mais detalhes.

## 🤝 Contribuição

Contribuições são bem-vindas! Por favor:
1. Faça um fork do projeto
2. Crie uma branch para sua feature
3. Commit suas mudanças
4. Abra um Pull Request

---

**Desenvolvido com ❤️ para a comunidade Discord**



