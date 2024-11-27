# Plano de Desenvolvimento de Pessoas (PDP)

O *Plano de Desenvolvimento de Pessoas (PDP)* é uma ferramenta estratégica para o planejamento e acompanhamento das competências, capacidades e habilidades a serem desenvolvidas pelos indivíduos e pelas instituições. Seu versionamento é anual, com base na identificação das necessidades organizacionais e individuais, visando alcançar metas e fortalecer o desempenho profissional.

### Estrutura e Finalidade do PDP
O PDP reúne informações importantes, como as necessidades de desenvolvimento, categorizadas por *eixos temáticos* e alinhadas a um público-alvo específico. Cada curso ou ação formativa vinculada ao PDP deve estar associada a pelo menos uma dessas necessidades.

Ao longo do ano, o PDP é utilizado para acompanhar a execução das iniciativas planejadas, e, ao final do período, serve como base para a elaboração de relatórios anuais. Esses relatórios incluem dados fundamentais, como:

-   *Quantidade de alunos*: diferenciando entre aqueles que participaram de cursos no Brasil e os que realizaram atividades no exterior.
-   *Carga horária total* dos cursos realizados.
-   *Quantidade de cursos associados ao PDP*, discriminando quais foram ofertados.
-   *Orçamento*: detalhamento de custos como diárias, passagens e outros gastos associados.
-   *Metas atingidas*, analisando o impacto e os resultados alcançados.


### Estrutura do Banco de Dados do PDP

Para a gestão eficiente das informações, a tabela de PDP possui os seguintes campos:

-   *ID do PDP*: id_pdp_pk (id_pk - UNIQUE).
-   *Número do PDP*: numero_pdp (int).
-   *Nome da necessidade*: nm_necessidade (varchar(255) ).
-   *Ano*: ano_pdp (int (4)).
-   *Eixo temático*: eixo_tematico (varchar(255) ).
-   *Alvo*: publico_alvo (varchar(100) ).

### Relacionamentos com Outras Tabelas

Os dados do PDP precisam ser integrados a tabelas relacionadas a diferentes tipos de cursos e licenças, como:

-   *Cursos*: cursos gerais oferecidos.
-   *Licença capacitação*: ações relacionadas a licenças para capacitação.
-   *Pós-graduação*: programas de pós-graduação.
-   *Cursos externos*: cursos realizados fora da instituição.
-   *Licença internacional*: licenças para capacitações no exterior.

Essas tabelas devem conter uma *chave estrangeira (FK)* para o campo correspondente ao *ID do PDP*. Essa abordagem centraliza as informações no PDP e permite rastrear facilmente os cursos e ações vinculadas a ele. Essa chave estrangeira ficaria idealmente nas tabelas dos cursos, para que cada curso ou licença possa estar vinculado a um PDP específico.
