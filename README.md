# 📘 Central de Conhecimento (ISP/Telecom)

Uma aplicação Web de página única (SPA) desenvolvida para gestão de conhecimento, procedimentos técnicos e suporte operacional. O sistema simula um ambiente corporativo de um provedor de internet (ISP), permitindo que atendentes e técnicos consultem soluções rápidas, contatos de emergência e scripts de atendimento.

![Status do Projeto](https://img.shields.io/badge/Status-Funcional-brightgreen) ![Tech](https://img.shields.io/badge/Tech-HTML%20%7C%20JS%20%7C%20Tailwind-blue)

## 🎯 Funcionalidades

### 🏢 Para o Usuário Comum (Atendentes/Técnicos)
* **Busca Inteligente:** Pesquisa em tempo real de artigos por título, conteúdo ou tags (ex: "lentidão", "los vermelho").
* **Base de Conhecimento:** Artigos divididos por setores (Suporte Técnico, Operacional) e categorias.
* **Scripts de Atendimento:** Visualização clara de "O que dizer ao cliente" e "Passo a passo técnico".
* **Contatos de Emergência:** Lista telefônica filtrável por equipe e cargo.
* **Cópia Rápida:** Botão para copiar scripts de resposta para a área de transferência.

### 🛡️ Para Administradores e Supervisores
* **Gestão de Usuários (CRUD):** Criar, editar, promover cargos e excluir usuários.
* **Gestão de Conteúdo (CRUD):** Editor completo para criar e atualizar procedimentos e artigos.
* **Gestão de Contatos:** Adicionar e remover telefones úteis da agenda.
* **Log de Auditoria e Reversão:**
    * Histórico detalhado de todas as ações (quem fez, o que fez e quando).
    * **Funcionalidade de Undo (Reverter):** Capacidade de desfazer alterações (ex: restaurar um artigo excluído ou reverter a edição de um usuário).
* **Segurança Extra:** Senha Mestra solicitada para ações críticas.

## 🚀 Tecnologias Utilizadas

O projeto foi construído como um **Monólito Front-end** (arquivo único) para facilidade de implantação e testes.

* **HTML5:** Estrutura semântica.
* **CSS3 & Tailwind CSS (via CDN):** Estilização moderna, responsiva e animações.
* **JavaScript (Vanilla):** Lógica de SPA, roteamento virtual, manipulação do DOM e "Mock Database".
* **Phosphor Icons:** Ícones vetoriais modernos.
* **Google Fonts:** Tipografia 'Inter'.

## 📦 Como Usar

Como o projeto utiliza CDNs e não requer build process, é extremamente simples de executar:

1.  Baixe o arquivo `index.html` (ou clone este repositório).
2.  Abra o arquivo diretamente em seu navegador (Chrome, Firefox, Edge).
3.  O sistema carregará automaticamente.

> **Nota:** O sistema utiliza um banco de dados em memória (`mockDB`). **Ao recarregar a página (F5), todas as alterações feitas (novos usuários, artigos editados) serão perdidas e os dados voltarão ao estado original.**

## 🔑 Credenciais de Acesso (Demo)

O sistema já vem populado com usuários de teste para diferentes níveis de acesso. Utilize as credenciais abaixo na tela de login:

| Usuário | Senha | Cargo | Nível de Acesso |
| :--- | :--- | :--- | :--- |
| **ana** | `123` | Atendente N1 | Básico (Leitura e Busca) |
| **bruno** | `123` | Supervisor | Intermediário (Gestão de Conteúdo) |
| **admin** | `admin` | Admin | Total (Gestão de Usuários e Histórico) |

### 🔐 Senha Mestra (Admin)
Para acessar áreas sensíveis (como a lista de usuários ou o histórico de edições), o sistema solicitará uma senha extra:
* **Senha Mestra:** `admin123`

## 📂 Estrutura do Código

O código está contido em um único arquivo HTML para portabilidade, organizado da seguinte forma:

1.  **`<head>`:** Importação de bibliotecas (Tailwind, Icons, Fonts) e CSS customizado (animações,
