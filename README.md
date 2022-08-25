### Construindo meu Primeiro Projeto de Banco de Dados
- **Projeto de Banco de Dados**
  - **Contexto:** Levantamento do Requisitos (Ordem de Serviço)
  - **Projeto Conceitual:** Modelo ER (Universidade)
  - **Projeto Lógico:** Modelo Relacional (E-Commerce)
  ---
 #### Modelando uma ordem de serviço

  **Contexto:**
  - Dentro de uma empresa os clientes demanda ao helpdesk algumas ações
  - Essas ações são convertidas em ordem de serviço
  - Os clientes realizam um pedido
  - O pedido é convertido em ordem de serviço caso possa ser realizado
  - O técnico executa a ordem de serviço. Após sua finalização a mesma é arquivada

  **Entidades:**
   - Cliente, Responsável, Pedido e Ordem de Serviço

  **Relacionamentos:**
   - Solicita, Analisa, Executa, Arquiva

  **Ferramenta de Desing alternativa**
   - Draw.io - Desing: [Union Type](/desafio-e-commerce-dio/union_type.drawio)
   - DBDesigner.net 

  **Instalando Workbench no Windows**
  - [MySQL Workbenck](https://www.mysql.com/products/workbench/)

  **Modelando o cenário de Ordem de Serviço**
  - [Ordem de Pedido](/desafio-e-commerce-dio/ordem.png)

  ---
#### Modelando um Cenánio de Universidade

  **Modelando Escopo de Universidade**
  - Projeto de Universidade: Qual o escopo? Ensino (Curso, Professor, Coordenação, Disciplina e Aluno)

  **Narrativa - Aluno**
  - A universidade possui diversos alunos que podem estar matriculados em mais de um curso (graduação)
  - Os alunos podem fazer cursos extras fornecidos externa e internamente (universidade) para contar como horas complementares
  - Não há restrição quanto ao número de matérias puxadas se não houver sobreposição de horário
  - Os alunos são submetidos a duas provas por semestre para cada disciplina. Eventuais trabalhos devem ser tratados pelo professor para compor a nota de prova

  **Narrativa - Disciplinas**
  - Cada disciplina é fornecida por um professor. Restrição: apenas por este professor
  - Algumas disciplinas possuem pré-requisitos. Um mesmo pré-requisito pode ser associado a mais de um disciplina
  - As disciplinas podem ser comuns a cursos distintos. Ex.: Cálculo 1 para computação e engenharia
  - O ciclo de vida da disciplina é semestral

  **Narrativa - Professores**
  - Os professores que ministram as disciplinas estão associados as coordenações de seus respectivos cursos. Ex.: Computação, Física, Engenharia...

  **Perguntas:**
  - Quais informações de aluno e professores guarda?
  - Qual média para aprovação?
  - Haverá restrição ou diferentes visões?

  **Modelando o cenário de Universidade**
  - [Cenário de Universidade](/desafio-e-commerce-dio/universidade.png)
  ---
#### Modelando um E-commerce

  **Projeto Ecommerce**
  - Qual o escopo? Venda de produtos (Produto, Estoque, Cliente, Pedido, Fornecedor)

  **Narrativa - Produto**
  - Os produtos são vendidos por uma única plataforma online. Contudo, estes podem ter vendedores distintos (terceiros)
  - Cada produto possui um fornecedor
  - Um ou mais produtos podem compor um pedido

  **Narrativa - Cliente**
  - O cliente pode se cadastrar no site com ceu CPF ou CNPJ
  - O endereço do cliente irá determinar o valor do frete
  - Um cliente pode comprar mais de um pedido. Este tem um período de carência para devolução do produto

  **Narrativa - Pedido**
  - Os pedidos são criados por clientes e possuem informações de compra, endereço e status da entrega
  - Um produto ou mais compoem o pedido
  - O pedido pode ser cancelado
  
  **Narrativa - Fornecedor e Estoque**
  - Vamos pensar juntos
  ---

#### Desafio 1: Replique e melhore!
  **Projeto de um E-commerce**
  **- Refinando**
  - Cliente PJ e PF - Uma conta pode ser PJ ou PF, mas não pode ter as duas informações
  - Pagamento - Pode ter cadastrado mais de uma forma de pagamento
  - Entrega - Possui status e código de rastreio

  **[E-commerce Refinado](/desafio-e-commerce-dio/e-commerce_Refinado.png)**
