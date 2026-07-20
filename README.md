# 🏡 Vesta

Uma app para planejar a casa, organizar o enxoval, acompanhar a obra e cuidar dos gastos em um só lugar.

🔗 **Acesse a prévia:**

<p align="center">
  <a href="https://samirasantos.github.io/Vesta/">
    <img src="https://img.shields.io/badge/🌺%20Abrir%20prévia%20online-Vesta-8F2A2A?style=for-the-badge&labelColor=F6EAD2&color=8F2A2A" alt="Abrir prévia online do Vesta" />
  </a>
</p>

O Vesta é um aplicativo em desenvolvimento criado para acompanhar pessoas durante a montagem de uma casa nova — desde os primeiros ambientes e itens do enxoval até compras, fornecedores, obra e organização financeira.

A ideia é transformar um processo que costuma ficar espalhado entre listas, anotações, planilhas e mensagens em uma experiência visual, acolhedora e simples de acompanhar.

## ✨ Sobre o projeto

O Vesta nasceu para reunir tudo o que faz parte da construção de um lar em um só lugar.

A proposta não é criar listas rígidas ou exigir que toda casa siga o mesmo modelo. Cada pessoa pode adaptar ambientes, prioridades, orçamento e itens à sua realidade, acompanhando o que já possui, o que ainda falta e o que está em andamento.

O projeto também conta com o Apolo, um assistente determinístico que ajuda a montar enxovais, organizar informações e registrar ações reais no sistema. Ele não utiliza modelos externos de inteligência artificial e sempre apresenta uma prévia antes de salvar alterações importantes.

## 🚧 Status do projeto

Este repositório é uma prévia pública do Vesta.

O aplicativo ainda está em desenvolvimento e suas funcionalidades continuam sendo ajustadas, testadas e melhoradas. Algumas telas, fluxos e regras podem mudar até a versão final.

## 🌿 Funcionalidades planejadas e em desenvolvimento

- Criação e organização de casas;
- Gestão de moradores e acesso compartilhado;
- Cadastro de ambientes;
- Planejamento completo de enxoval;
- Controle de itens existentes, desejados e comprados;
- Registro de compras, parcelas, frete e descontos;
- Comparação e monitoramento de preços;
- Organização de obras e reformas;
- Cadastro de fornecedores e orçamentos;
- Controle financeiro de enxoval, obra e gastos avulsos;
- Histórico de atividades;
- Assistente Apolo para ações guiadas;
- Experiência responsiva para desktop e mobile.

## 🏠 Alguns módulos do Vesta

### Visão geral

Um resumo da casa atual, com progresso, pendências, gastos e atalhos para as áreas mais importantes.

### Enxoval

Espaço para montar listas por ambiente, acompanhar quantidades, definir prioridades e registrar o que já foi comprado.

### Ambientes

Organização dos cômodos da casa e dos itens relacionados a cada espaço.

### Obra

Área para planejar reformas, etapas, materiais, serviços, fornecedores, orçamentos e pagamentos.

### Financeiro

Visão concentrada nos gastos relacionados ao enxoval, à obra e em despesas avulsas que a pessoa queira registrar.

### Apolo

Assistente do Vesta que conduz perguntas objetivas, prepara rascunhos e executa ações reais somente depois da confirmação do usuário.

## 🔎 Pesquisa e monitoramento de preços

O Vesta possui uma base para comparação e acompanhamento de ofertas.

Depois que um produto passa a ser monitorado, seus links ficam registrados para novas consultas. Os preços exibidos representam o momento da coleta e sempre devem ser confirmados na loja antes da compra.

## 🎨 Identidade visual

O Vesta possui uma estética acolhedora, leve e ligada à ideia de casa, com inspiração em:

- tons naturais;
- verde escuro e bege;
- organização doméstica;
- interiores;
- materiais e texturas suaves;
- interfaces limpas e confortáveis.

A proposta visual é transmitir tranquilidade sem perder clareza, hierarquia ou usabilidade.

## 🛠️ Tecnologias

O projeto está sendo desenvolvido com:

- React;
- TypeScript;
- Vite;
- Tailwind CSS;
- Supabase;
- PostgreSQL;
- Vitest;
- Node.js.

## 💻 Desenvolvimento local

### Requisitos

- Node.js 20.18 ou mais recente;
- npm 10 ou mais recente;
- um projeto Supabase.

### Instalação

```powershell
git clone https://github.com/SamiraSantos/Vesta.git
cd Vesta
npm install
Copy-Item .env.example .env
npm run dev
```

Preencha o `.env` com a URL e a chave pública do seu projeto Supabase:

```dotenv
VITE_SUPABASE_URL=https://SEU_PROJECT_REF.supabase.co
VITE_SUPABASE_PUBLISHABLE_KEY=sb_publishable_SUBSTITUA_AQUI
```

Nunca coloque `service_role`, secret keys, senhas ou tokens privados em variáveis com o prefixo `VITE_`.

### Banco de dados

As migrations ficam em `supabase/migrations`.

```powershell
npx supabase link --project-ref SEU_PROJECT_REF
npx supabase db push --dry-run
npx supabase db push
```

Revise o `dry-run` antes de aplicar qualquer migration em um projeto remoto.

### Qualidade

```powershell
npm run typecheck
npm run lint
npm test
npm run db:check-syntax
npm run build
```

## 📱 Prévia

Esta versão pública representa o Vesta em construção.

Ela serve para apresentar a proposta visual, os fluxos principais e a ideia de centralizar o planejamento da casa. O projeto ainda não representa a versão final do produto.

## 🔒 Privacidade e segurança

O Vesta lida com informações pessoais, financeiras e relacionadas à residência.

Por isso, o projeto foi estruturado com foco em:

- autenticação individual;
- isolamento dos dados por usuário e casa;
- Row Level Security no Supabase;
- arquivos privados;
- confirmação antes de ações importantes;
- ausência de chaves administrativas no frontend;
- controle do usuário sobre os próprios registros.

Na configuração atual de desenvolvimento, a confirmação de e-mail no cadastro está desativada. Isso simplifica os testes da prévia e deve ser reavaliado antes de uma publicação aberta em produção.

## 🧪 Em desenvolvimento

O projeto ainda está passando por:

- ajustes de interface;
- melhorias de experiência mobile;
- correções de bugs;
- revisão de segurança;
- testes de regras de negócio;
- refinamento do Apolo;
- evolução do monitoramento de preços;
- organização e otimização do banco de dados.

## 🤍 Observação

Este repositório é uma prévia pública e pode não conter todas as funcionalidades, regras de negócio ou integrações previstas para a versão final.

O Vesta ainda está sendo construído, um ambiente de cada vez. 🌿
