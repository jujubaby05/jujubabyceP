# 📚 Guia Completo: Deploy no GitHub e Netlify

## Sumário
1. [Preparação](#preparação)
2. [Fazer Upload para GitHub](#fazer-upload-para-github)
3. [Conectar ao Netlify](#conectar-ao-netlify)
4. [Atualizar o Site](#atualizar-o-site)

---

## Preparação

### Pré-requisitos
- ✅ Git instalado (você já tem!)
- ✅ Conta no GitHub (jujubaby05)
- ✅ Repositório criado: `https://github.com/jujubaby05/jujubabyceP`
- ✅ Conta no Netlify

### Informações Importantes
- **Username GitHub:** jujubaby05
- **Email:** 0d5a6d@gmail.com
- **Repositório:** https://github.com/jujubaby05/jujubabyceP

---

## Fazer Upload para GitHub

### Passo 1: Abrir o Terminal/CMD

1. Abra o **Explorador de Arquivos** do Windows
2. Navegue até a pasta do seu projeto
3. Clique na barra de endereço e digite `cmd`
4. Pressione Enter

**Ou:**
- Clique com botão direito na pasta → "Abrir terminal aqui"

### Passo 2: Configurar Git (primeira vez apenas)

Execute esses comandos **uma única vez**:

```bash
git config --global user.name "jujubaby05"
git config --global user.email "0d5a6d@gmail.com"
```

### Passo 3: Inicializar o Repositório Local

Na pasta do seu projeto, execute:

```bash
git init
```

Isso cria um repositório Git local.

### Passo 4: Adicionar Todos os Arquivos

```bash
git add .
```

Isso prepara todos os arquivos para serem enviados.

### Passo 5: Fazer o Primeiro Commit

```bash
git commit -m "Inicial: JuJuBaBy CEP com novo branding"
```

### Passo 6: Conectar ao Repositório Remoto

```bash
git branch -M main
git remote add origin https://github.com/jujubaby05/jujubabyceP.git
```

### Passo 7: Fazer Push (Enviar para GitHub)

```bash
git push -u origin main
```

**Atenção:** Você será pedido para fazer login. Siga as instruções na tela.

---

## Conectar ao Netlify

### Passo 1: Acessar o Netlify

1. Acesse: https://app.netlify.com
2. Faça login com sua conta

### Passo 2: Criar Novo Site

1. Clique em **"Add new site"**
2. Selecione **"Import an existing project"**
3. Clique em **"GitHub"**

### Passo 3: Autorizar o Netlify

1. Clique em **"Authorize Netlify"**
2. Faça login no GitHub
3. Autorize o Netlify a acessar seus repositórios

### Passo 4: Selecionar Repositório

1. Procure por **"jujubabyceP"** na lista
2. Clique nele para selecionar

### Passo 5: Configurar Build

A página deve mostrar:
- **Build command:** `npm run build`
- **Publish directory:** `dist`

Se não aparecer, configure manualmente:

1. Clique em **"Deploy site"** (ou configure antes)
2. Espere o build terminar (pode levar 2-5 minutos)

### Passo 6: Pronto! 🎉

Seu site estará online em um URL como:
- `https://jujubabyceP.netlify.app`

---

## Atualizar o Site

Sempre que você fizer mudanças no projeto, siga esses passos:

### Passo 1: Abrir o Terminal na Pasta do Projeto

```bash
cd C:\caminho\para\seu\projeto
```

### Passo 2: Adicionar as Mudanças

```bash
git add .
```

### Passo 3: Fazer Commit

```bash
git commit -m "Descrição da mudança"
```

**Exemplos:**
- `git commit -m "Atualizar cores da etiqueta"`
- `git commit -m "Corrigir cálculo de frete"`
- `git commit -m "Adicionar novo CEP padrão"`

### Passo 4: Fazer Push

```bash
git push
```

**Pronto!** O Netlify detectará a mudança automaticamente e atualizará seu site em poucos minutos.

---

## Comandos Rápidos

### Ver Status
```bash
git status
```

### Ver Histórico de Commits
```bash
git log
```

### Desfazer Mudanças
```bash
git restore .
```

### Clonar o Repositório em Outro Computador
```bash
git clone https://github.com/jujubaby05/jujubabyceP.git
cd jujubabyceP
npm install
npm run dev
```

---

## Troubleshooting

### Erro: "fatal: not a git repository"
**Solução:** Execute `git init` na pasta do projeto

### Erro: "Permission denied"
**Solução:** Verifique se você está logado no GitHub. Execute:
```bash
git config --global user.name "jujubaby05"
git config --global user.email "0d5a6d@gmail.com"
```

### Erro: "branch 'main' set up to track 'origin/main'"
**Solução:** Tudo OK! Isso é normal na primeira vez.

### Site não atualiza no Netlify
**Solução:** 
1. Verifique se o push foi bem-sucedido: `git log`
2. Verifique o build no Netlify: Site → Deploys
3. Espere 5 minutos e recarregue a página

---

## Próximos Passos

Agora que seu site está online, você pode:

1. ✅ Compartilhar a URL com clientes
2. ✅ Adicionar domínio customizado (Netlify → Domain settings)
3. ✅ Configurar SSL/HTTPS (automático no Netlify)
4. ✅ Monitorar analytics (Netlify → Analytics)

---

## Dúvidas?

Se tiver dúvidas, releia este guia ou me contacte! 👍

**Resumo dos comandos principais:**
```bash
# Primeira vez
git init
git config --global user.name "jujubaby05"
git config --global user.email "0d5a6d@gmail.com"
git add .
git commit -m "Inicial"
git branch -M main
git remote add origin https://github.com/jujubaby05/jujubabyceP.git
git push -u origin main

# Próximas atualizações
git add .
git commit -m "Descrição da mudança"
git push
```

Boa sorte! 🚀
