# Adopet

O **Adopet** é um projeto feito para praticar integrar TypeScript em um projeto anterior JavaScript, ele é uma plataforma fictícia e sem fins lucrativos que conecta pessoas que desejam adotar animais de estimação com ONGs e cuidadores. O sistema permite a visualização de pets disponíveis, cadastro de usuários, autenticação e envio de mensagens para os responsáveis pelos animais.

Ele facilita o processo de adoção responsável. Através de uma interface amigável e direta, os usuários podem navegar por uma lista de animais que precisam de um lar, verificar seus detalhes (como porte, idade, localização e descrição) e entrar em contato direto com a instituição ou pessoa responsável. 

Este projeto foi desenvolvido como uma Single Page Application (SPA) moderna, focada em performance, componentização e tipagem estática para garantir a segurança e manutenção do código. Ele utiliza um servidor local simulado (JSON Server) para emular o comportamento de uma API real de adoção e gerenciamento de usuários.

## Funcionalidades

- **Listagem de Pets:** Visualização em cards dos animais disponíveis para adoção.
- **Autenticação de Usuários:** Fluxo completo de Login e Cadastro (Sign In / Sign Up).
- **Gestão de Perfil:** Os usuários podem visualizar e editar seus dados pessoais (nome, email, telefone, cidade e um texto "sobre").
- **Contato Responsável:** Formulário dedicado para enviar mensagens de interesse aos cuidadores dos pets.
- **Rotas Privadas:** Proteção de rotas, exigindo login para acessar a página inicial e detalhes da adoção.

## Tecnologias Utilizadas

Este projeto foi desenvolvido com as seguintes tecnologias:

- **[React 19](https://react.dev/):** Biblioteca principal para construção da interface.
- **[TypeScript](https://www.typescriptlang.org/):** Adicionando tipagem estática ao JavaScript.
- **[Vite](https://vitejs.dev/):** Ferramenta de *build* super rápida.
- **[Tailwind CSS v4](https://tailwindcss.com/):** Framework utilitário para estilização e responsividade.
- **[React Router v7](https://reactrouter.com/):** Gerenciamento de rotas e navegação da aplicação.
- **[JSON Server](https://github.com/typicode/json-server):** Simulação de uma API REST completa baseada no arquivo `server.json`.
- **[Simple Auth Storage](https://www.npmjs.com/package/simple-auth-storage):** Gerenciamento simplificado de token e estado de autenticação no front-end.

## Como executar o projeto

Para rodar a aplicação localmente, você precisará ter o [Node.js](https://nodejs.org/) instalado na sua máquina.

**1. Clone o repositório:**
```bash
git clone https://github.com/seu-usuario/adopet.git
cd adopet
```
2. Instale as dependências:
```bash
npm install
# ou
yarn install
```
3. Inicie o servidor local (API Mockada):
Em um terminal, rode o comando abaixo para iniciar o json-server na porta 3001:
```bash
npm run server
```
4. Inicie o Front-end:
Em outro terminal (mantendo o servidor da API rodando), inicie o Vite:
```bash
npm run dev
```
A aplicação estará disponível em http://localhost:5173/ (ou a porta indicada pelo Vite no terminal).

## Estrutura de Pastas
A estrutura do projeto foi pensada para ser escalável e fácil de manter:
```text
src/
├── assets/         # Imagens, ícones e arquivos estáticos (logos, svgs)
├── components/     # Componentes reutilizáveis (Button, Card, Header, Input, etc)
├── contexts/       # Context API para gerenciamento de estado global (Pets e Users)
├── pages/          # Páginas da aplicação (Home, Contact, Profile, SignInUp, NotFound)
├── routes/         # Configuração do React Router (index.tsx)
├── types/          # Definições de interfaces e tipos globais do TypeScript
├── utils/          # Funções utilitárias (como a função genérica fetchData)
├── index.css       # Configurações globais e injeção do Tailwind
└── main.tsx        # Ponto de entrada principal da aplicação React
```
