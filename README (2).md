# DJ Gato Félix - Sistema de Gerenciamento de Eventos

Sistema de gerenciamento de agenda e eventos para o DJ Gato Félix, com funcionalidades para controle de agenda, contatos, locais e relatórios.

## Funcionalidades

- Gerenciamento de eventos com contagem regressiva
- Cadastro e organização de contatos
- Cadastro de locais para eventos
- Calendário mensal interativo 
- Geração e envio de relatórios por email
- Interface completamente traduzida para português (incluindo Dashboard, Contatos, Locais, Calendário)

## Requisitos

- Node.js (v16+)
- npm ou yarn

## Instalação

1. Clone o repositório:
```bash
git clone https://github.com/seu-usuario/dj-gato-felix.git
cd dj-gato-felix
```

2. Instale as dependências:
```bash
npm install
```

3. Inicie o projeto:
```bash
npm run dev
```

4. Acesse no navegador:
```
http://localhost:5000
```

## Tecnologias Utilizadas

- React.js (Frontend)
- Express.js (Backend)
- TanStack Query para gestão de estado
- Tailwind CSS + shadcn/ui para componentes e estilização
- Sistema de armazenamento em memória (pode ser expandido para uso com PostgreSQL)

## Estrutura do Projeto

- `/client` - Código frontend em React
  - `/src/components` - Componentes reutilizáveis
  - `/src/pages` - Páginas da aplicação
  - `/src/lib` - Utilitários e configurações
  - `/src/hooks` - Hooks personalizados

- `/server` - Código backend em Express
  - `routes.ts` - Rotas da API
  - `storage.ts` - Sistema de armazenamento de dados
  
- `/shared` - Código compartilhado entre frontend e backend
  - `schema.ts` - Definição dos esquemas de dados

## Versão de Demonstração e Implantação no GitHub Pages

O projeto possui duas versões:

### 1. Versão Completa (Desenvolvimento Local)
Ao executar localmente com `npm run dev`, a aplicação utiliza o backend completo com as funcionalidades:
- Armazenamento em memória para todos os dados
- API completa para manipulação de eventos, contatos e locais
- Geração de relatórios

### 2. Versão de Demonstração (GitHub Pages)
Quando hospedado no GitHub Pages, o sistema funciona em modo de demonstração:
- Utiliza dados pré-configurados em memória
- Simula operações de API no frontend
- Permite visualizar e testar a interface sem necessidade de um servidor backend

#### Como implantar no GitHub Pages (específico para o repositório gogo):

1. Baixe o projeto completo do Replit
2. Execute o script de build para GitHub Pages (que foi atualizado para o seu repositório 'gogo'):
   ```bash
   bash build-github.sh
   ```
3. Faça upload do conteúdo da pasta `dist` (não mais `build`) para seu repositório GitHub
4. Vá para as configurações do repositório
5. Na seção "GitHub Pages", selecione a branch `main` como fonte e a pasta `/dist` se estiver fazendo upload de todo o projeto
6. Ou crie uma branch `gh-pages` apenas com o conteúdo da pasta `dist`
7. O site estará disponível após alguns minutos em: `https://cheerfull001.github.io/gogo/`

#### Para atualizar um repositório existente:

1. Baixe os arquivos mais recentes do Replit
2. Execute o script de build para GitHub Pages
3. Substitua os arquivos no seu repositório GitHub pelos da pasta `dist`
4. Faça commit e push das alterações

#### Arquivos Especiais para GitHub Pages:

- O arquivo `.nojekyll` garante que o GitHub Pages não tente processar o site como um projeto Jekyll
- O arquivo `index.html` na raiz inclui lógica de redirecionamento específica para GitHub Pages
- O arquivo `client/src/demoData.ts` contém os dados de demonstração
- O arquivo `client/src/lib/queryClient.ts` foi modificado para usar dados de demonstração quando executado no GitHub Pages
- O arquivo `404.html` na raiz permite navegação direta para rotas dentro do aplicativo

## Status da Tradução

O projeto está sendo completamente traduzido para o português. Atualmente, as seguintes partes já estão traduzidas:

- ✅ Barra lateral de navegação
- ✅ Dashboard (Página inicial)
- ✅ Contatos
- ✅ Locais
- ✅ Calendário
- ✅ Formulário de Eventos
- ⏳ Relatórios (em andamento)
- ⏳ Configurações (em andamento)

## Licença

Este projeto está licenciado sob a Licença MIT.