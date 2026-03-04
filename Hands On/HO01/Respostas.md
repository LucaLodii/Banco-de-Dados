# Respostas - HO01: Fundamentos em Banco de Dados

1. **O que é um sistema de banco de dados (SBD)?**
   Sistemas de banco de dados referem-se ao conjunto de dados relacionados e sua respectiva forma de acesso e organização. São compostos por uma coleção de dados organizados, uma estrutura lógica determinando a forma como os dados são armazenados, organizados e manipulados, e um software que provê acesso aos dados a usuários e aplicações.

2. **Do que um SBD é composto?**
   - **Coleção de Dados** -> Banco de Dados
   - **Estrutura Lógica** -> Modelos de dados
   - **Software** -> SGBD

3. **Como usuários e aplicações interagem com um SBD?**
   Usuários e aplicações interagem com banco de dados por meio de queries SQL.

4. **O que é um banco de dados (BD)? Cite um exemplo de um BD, indicando o link onde seja possível encontrá-lo.**
   Um banco de dados é uma coleção de dados relacionados. Um exemplo de software SGBD (comumente chamado de BD) é o MySQL.
   Link: [https://www.mysql.com/](https://www.mysql.com/)

5. **Quais são as propriedades de um BD?**
   - Um banco de dados representa algum aspecto do mundo real, às vezes chamado de "miniworld" ou "universe of discourse".
   - Um banco de dados é uma coleção logicamente coerente de dados com um significado. Uma coleção aleatória de dados não pode ser chamada de banco de dados.
   - Um banco de dados é montado e populado com dados para um propósito específico.

6. **Quais são as etapas de um projeto de BD?**
   - Especificação
   - Análise de requisitos 
   - Projeto conceitual
   - Projeto lógico
   - Projeto físico

7. **O que é um sistema gerenciador de banco de dados (SGBD)?**
   Um SGBD é uma ferramenta que permite adicionar, remover, atualizar e ler dados de um banco de dados de forma facilitada.

8. **Quais são as propriedades de um SGBD?**
   Controle de redundância, flexibilidade, economia de escala, alta disponibilidade, tempo de desenvolvimento de aplicação reduzido e capacidade de representação de relacionamento entre dados complexos no banco de dados.

9. **Indique situações em que o uso de SGBD pode se mostrar inadequado.**
   Pela natureza dos SGBDs serem ferramentas generalistas, seu uso pode ser inadequado quando operações muito específicas e de baixíssima latência são necessárias, ou quando o custo/complexidade não justifica o uso para dados extremamente simples.

10. **O que é um modelo de dados?**
    Modelos de dados servem para refletir a estrutura do banco de dados e o que o compõe. Inclui ferramentas para inserir, remover, modificar e recuperar dados.

11. **Em relação ao nível de abstração, quais são os tipos de modelos de dados?**
    - **Conceitual:** maior nível de abstração.
    - **Representativo (ou Lógico):** nível médio de abstração.
    - **Físico:** nível baixo de abstração.

12. **O que é um Esquema de BD?**
    Um esquema é uma descrição do BD em forma de metadados (a estrutura definida).

13. **O que é uma Instância de BD?**
    Uma instância é o conteúdo do BD em um momento específico (os dados reais num dado instante).

14. **Quais as vantagens de se adotar uma Arquitetura de Três Esquemas para implementar um BD?**
    A arquitetura de três esquemas permite a visualização facilitada para o usuário com autodescrição, suporte a múltiplas visões e, principalmente, a independência de dados.

15. **Quais níveis existem em uma Arquitetura de Três Esquemas?**
    - **Nível Externo:** descreve a parte do banco de dados que interessa a um grupo de usuários, ocultando o restante.
    - **Nível Conceitual:** descreve a estrutura de todo o banco de dados (entidades, relacionamentos, restrições).
    - **Nível Interno:** descreve o armazenamento físico e caminhos de acesso aos dados.

16. **O que é Mapeamento em uma Arquitetura de Três Esquemas?**
    Mapeamento é o processo de transformar requisições e resultados entre os diferentes níveis da arquitetura.

17. **O que é Independência de Dados e qual sua importância para um SBD?**
    É a capacidade de alterar o esquema em um nível sem precisar alterar o esquema no nível superior (ex: mudar o armazenamento físico sem quebrar a aplicação).

18. **O que é uma Linguagem de Consulta?**
    São linguagens do banco de dados (como VDL, DDL, SDL e DML) que provêem as ferramentas para realizar operações e consultas no BD.

19. **Cite as linguagens incorporadas na linguagem SQL.**
    O SQL incorpora linguagens como DDL (Data Definition Language) e DML (Data Manipulation Language). Exemplos de sistemas que a utilizam são MySQL, Postgres e SQLite.
