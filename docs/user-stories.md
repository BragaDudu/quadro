# User stories — O Quadro

## US-01 — Ver quem pegou cada tarefa

**Contexto:** ela chega no escritório às 8h e tem que procurar alguma tarefa dentro do zap desorganizado, que todos jogam as tarefas sem nenhuma organização. Quando ela acha uma tarefa perdida, acha que está pendente ainda e começa a realizar a mesma. Depois de algumas horas ela termina a tarefa e descobre que essa tarefa já tinha sido finalizada por outro dev, o que fez ela perder tempo e qualidade, pois todo dia é essa mesma coisa e ela acaba se desgastando.

**Como** Lia, **quero** ver quem já pegou cada tarefa, **para** não perder horas realizando uma tarefa que outro dev já concluiu. Assim ela consegue ver quais tarefas ainda estão pendentes e se tornar responsável por aquela pendência.

**Critérios de aceite**
- **Dado** uma tarefa que o Pedro já pegou e uma que ninguém pegou, **quando** a Lia abre o quadro, **então** ela vê o nome "Pedro" na primeira e "sem dono" na segunda.
- **Dado** uma tarefa que já tem o Pedro como responsável, **quando** a Lia tenta pegar essa tarefa, **então** ela não consegue, pois aquela tarefa já tem um responsável.

---

## US-02 — Ver tarefas concluídas e pendentes

**Contexto:** o Otávio recebe as tarefas da Rê, porém joga desorganizadamente dentro do grupo do zap da Faro Labs. Como é tudo desorganizado, ele mesmo acaba se complicando e às vezes não consegue revisar um PR, ou até mesmo não consegue ver quais tarefas que a Rê passou estão pendentes ou ainda não.

**Como** Otávio, **quero** ver quais tarefas foram concluídas e quais não foram ainda, **para** conseguir ter um controle e se organizar no dia a dia com as tarefas passadas pela Rê. Assim ele consegue saber quem cobrar ou até mesmo ter um controle maior para revisar os PRs.

**Critérios de aceite**
- **Dado** que existem 1 tarefa pendente, 2 em andamento e 3 finalizadas, **quando** o Otávio abre o quadro, **então** ele lê na tela quais tarefas ainda estão pendentes, quais estão em andamento e quais já estão finalizadas.
- **Dado** que nenhuma tarefa foi concluída ainda, **quando** o Otávio abre o quadro, **então** ele vê a mensagem "nenhuma tarefa concluída ainda".

---

## US-03 — Acompanhar as tarefas sem saber código

**Contexto:** a Rê, uma cliente da Faro Labs, manda as tarefas pro Otávio, porém está bem insatisfeita, pois nada é organizado dentro da Faro e ela não sabe qual tarefa está pronta, ou quem fez, ou até mesmo se o Otávio anotou o pedido dela ou não.

**Como** Rê, **quero** saber quando as tarefas foram finalizadas ou não foram feitas ainda, e entender mesmo não sabendo nada de código, **para** poder me despreocupar com a parte de desenvolvimento e focar em outras áreas, como vendas e marketing, sem perder tempo. Então ela consegue ver no quadro, ao final do dia, todas as tarefas que passou para o Otávio e se estão feitas ou não.

**Critérios de aceite**
- **Dado** as tarefas que a Rê passou para o Otávio, **quando** ela abre o quadro, **então** ela vê quais estão pendentes, quais estão em andamento e quais estão finalizadas.
- **Dado** que a Rê é uma "leitora", **quando** ela tenta mover uma tarefa, **então** ela não consegue mover nada.
