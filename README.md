# JuJuBaBy CEP - Sistema de Cálculo de Frete

Sistema profissional para cálculo de frete dos Correios e geração de etiquetas em PDF com branding JuJuBaBy.

## Funcionalidades

- ✅ Cálculo de frete PAC e SEDEX (simulação)
- ✅ Consulta automática de CEP via ViaCEP
- ✅ Criação de etiquetas profissionais (10x15cm)
- ✅ Geração de PDF para impressão
- ✅ Pré-visualização em tempo real
- ✅ Formato individual e folha A4 (até 4 etiquetas)
- ✅ Interface moderna e responsiva
- ✅ CEP padrão: 79017-121 (Campo Grande - MS)

## Como usar localmente

```bash
# Instalar dependências
npm install
# ou
pnpm install

# Rodar em desenvolvimento
npm run dev
# ou
pnpm dev

# Gerar build de produção
npm run build
```

## Deploy no Netlify (Recomendado)

### Via GitHub (Automático)

1. Faça upload deste projeto para seu repositório no GitHub
2. Acesse [netlify.com](https://netlify.com) e faça login
3. Clique em "Add new site" → "Import an existing project"
4. Selecione "GitHub"
5. Escolha o repositório `jujubabyceP`
6. Clique em "Deploy site"
7. Pronto! Seu site estará online em poucos minutos

### Configurações do Netlify

**Build command:** `npm run build` ou `pnpm build`  
**Publish directory:** `dist`

Após conectar, qualquer push no repositório GitHub atualizará automaticamente seu site!

## Deploy na Vercel

1. Acesse [vercel.com](https://vercel.com) e faça login com sua conta GitHub
2. Clique em "Add New Project"
3. Selecione o repositório `jujubabyceP`
4. Clique em "Deploy"
5. Pronto! Seu site estará online

## Configurações de Frete

As configurações de frete estão no arquivo `src/App.tsx` na constante `CONFIG`:

```typescript
const CONFIG = {
  taxaFixa: 5.00,              // Taxa fixa por envio
  margemPercentual: 10,        // Margem de lucro em %
  pesoMinimo: 300,             // Peso mínimo em gramas
  precoPAC: 18.50,             // Preço base PAC por kg
  precoSEDEX: 32.00,           // Preço base SEDEX por kg
  prazoPAC: 8,                 // Prazo base PAC em dias
  prazoSEDEX: 3,               // Prazo base SEDEX em dias
  cepPadraoOrigem: '79017-121' // CEP padrão (Campo Grande - MS)
};
```

Ajuste esses valores conforme sua necessidade e faça um novo deploy.

## Estrutura do Projeto

```
jujubabyceP-deploy/
├── src/
│   ├── App.tsx          # Componente principal
│   ├── index.css        # Estilos globais
│   └── main.tsx         # Ponto de entrada
├── public/              # Arquivos estáticos
├── package.json         # Dependências
├── vite.config.ts       # Configuração Vite
└── README.md            # Este arquivo
```

## Tecnologias

- React 18 + TypeScript
- Vite
- Tailwind CSS
- jsPDF (geração de PDF)
- Lucide React (ícones)

## Atualizações Recentes

- ✨ Novo branding: JuJuBaBy CEP
- 🎨 Etiquetas redesenhadas (profissional)
- 📍 CEP padrão: 79017-121 (Campo Grande - MS)
- 🔄 Pré-visualização em tempo real
- 📄 Suporte a múltiplas etiquetas por folha

## Suporte

Para dúvidas ou problemas, verifique:
1. Se o Node.js está instalado (`node --version`)
2. Se as dependências foram instaladas (`npm install`)
3. Se a porta 5173 está disponível

## Licença

MIT
