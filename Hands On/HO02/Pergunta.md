# Hands-On

Esta é a tarefa **HO02: Modelagem Conceitual**, uma atividade prática que estimula o aluno a modelar conceitualmente bancos de dados.

## Problema

Gerar um modelo conceitual representado como um diagrama entidade-relacionamento (DER) usando a notação de **Peter Chen** a partir da seguinte descrição de minimundo:

### Minimundo: SAM (v1.0)
O **SAM (Sistema Acadêmico de Matrículas)** gerencia a matrícula de alunos em cursos em instituições de ensino. 

- **Áreas de Conhecimento:** Os cursos são categorizados por áreas. Um curso obrigatoriamente pertence a uma área e uma área pode possuir vários cursos. Uma área pode ser integrada por outras áreas (auto-relacionamento), sendo que uma área só pode ser integrante de uma única área. Áreas têm **sigla** (ID) e **nome**.
- **Cursos:** Identificados por **sigla**. Possuem **nome**, **custo** e **professores** (compostos por CPF e nome). 
- **Alunos:** Identificados por **CPF**. Possuem **nome** (composto de primeiro nome e sobrenome), **sexo** e **data de nascimento**.
- **Matrículas:** Cada aluno pode se matricular em diversos cursos, e vice-versa. Deve-se registrar a **data** e o status de **pagamento**.
- **Módulos:** Cada curso é composto por módulos. Um módulo pertence a apenas um curso (dependência existencial). Identificados por **sigla** e possuem **nome**.
- **Tópicos:** Cada módulo é composto por tópicos. Um tópico só existe em função de um módulo. Identificados por **sigla** e possuem **nome** e **horas**.
- **Atributo Derivado:** As horas do curso são derivadas da totalização das horas dos tópicos que compõem seus módulos.

## Produto
O aluno deve entregar um documento exclusivamente no formato **PDF** contendo a solução para o problema descrito anteriormente.

## Recursos
Para a execução da tarefa o aluno deve consultar as referências bibliográficas especificadas no Programa do Curso.

### Livro (Elmasri & Navathe, 2016):
- **Capítulo 3:** Modelagem de Dados usando o Modelo Entidade-Relacionamento (ER)

### Slides e Videos:
- **Tópico #04:** Modelo ER  
- **Tópico #05:** Modelo EER