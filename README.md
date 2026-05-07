# LegisDoc Keep Alive

Este repositório contém uma automação (GitHub Actions) para manter o backend do **LegisDoc** ativo no Render, evitando a hibernação automática do plano gratuito.

## Como funciona?

- O script envia uma requisição (ping) para `https://legisdoc.onrender.com/` a cada **14 minutos**.
- A automação está configurada para rodar apenas entre **06:00 e 22:00 (Horário de Brasília)** para economizar sua cota de minutos do GitHub Actions.

## Como ativar?

1. Crie um novo repositório **público** ou **privado** no seu GitHub chamado `LegisDoc-KeepAlive`.
2. Siga as instruções do GitHub para enviar estes arquivos para lá:
   ```bash
   git init
   git add .
   git commit -m "feat: adicionar automação keep-alive"
   git branch -M main
   git remote add origin https://github.com/SEU_USUARIO/LegisDoc-KeepAlive.git
   git push -u origin main
   ```
3. Assim que o código subir, vá na aba **Actions** do seu repositório no GitHub para ver o robô funcionando.
