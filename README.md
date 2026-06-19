<div align="center">
 
 # Delicia-Gelada-BANCO_DE_DADOS
</div>

> **Projeto Integrado** — SENAI Jandira | Curso Técnico em Desenvolvimento de Sistemas  
> **Empresa / Equipe:** Fynix

---

## 1. Descrição do Repositório

Esse repositório tem como objetivo armazenar os arquivos do banco de dados do projeto integrado, tanto o conceitual quanto o lógico e principalmente o script, para que os professores possam tem uma visão mais clara de como está o andamento da parte de DB do projeto.
---

<img align="right" alt="modelo conceitual" src="img/imagem do banco conceitual.png" width="500">
O diagrama ilustra o fluxo principal da plataforma, onde a entidade Cliente (representando os usuários que passam pela validação de maioridade e acessam a vitrine) realiza um Cadastro único e obrigatório (1,1) no sistema. A partir desse registro, estabelece-se uma relação (0,n) com a entidade Produto (as bebidas alcoólicas e não alcoólicas comercializadas). Os atributos do cliente cobrem a autenticação e perfil (id, nome, email, senha, foto, cargo). Já os atributos do produto sustentam os requisitos da landing page e catálogo, armazenando informações essenciais para a vitrine virtual (nome, preco, descricao, imagem, categoria, status_produto, tipo_bebida).

<br>
</br>

<img align="left" alt="modelo lógico" src="img/imagem do banco logico.png" width="500">
Esta modelagem reflete diretamente os requisitos de controle de estoque e o escopo do Painel Administrativo (CRUD). Para evitar redundâncias, a arquitetura foi dividida em tabelas especializadas conectadas por chaves estrangeiras (FK). A tabela principal de produtos (tbl_bebida) centraliza os dados comerciais (como preco e imagem) e herda relacionamentos de tabelas auxiliares que organizam o catálogo: tbl_categoria_bebida e tbl_tipo_bebida (permitindo a separação entre alcoólicos e não alcoólicos). A tabela tbl_usuario armazena os dados de acesso e está vinculada à tabela tbl_cargo, o que garante o controle de permissões necessário para diferenciar um cliente comum de um gestor que opera o CRUD administrativo.
