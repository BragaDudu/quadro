# Spec — US-01: Ver quem pegou cada tarefa

## Objetivo (1 frase)
A Lia consegue ver quem é responsável por cada tarefa, para não perder tempo e pegar uma tarefa que ninguém é responsável ainda.

## Contexto
A Labs é uma software house que tem uma cliente, a Rê, que tem uma loja. Ela passa as tarefas pro tech lead dentro do grupo do zap, porém o tech lead e os devs ficam sem organização, então às vezes dois devs resolvem o mesmo bug e depois descobrem que o outro já tinha feito.

Quem usa esta parte: a Lia (dev júnior), que quer ver quem já pegou cada tarefa para não perder horas realizando uma tarefa que outro dev já concluiu.

## O que deve acontecer (passo a passo)
1. A Lia abre o quadro e escolhe o próprio nome numa lista de nomes (sem senha).
2. Ela vê quais tarefas estão pendentes, fazendo, pra revisão e feitas, e em cada tarefa o nome do responsável ou "sem dono".
3. Ela escolhe uma tarefa sem responsável da coluna "A fazer" e atribui a ela.
4. A tarefa passa a mostrar que ela é responsável.

## Regras e casos de erro
- Somente uma pessoa pode ficar responsável por tal tarefa.
- Se a tarefa já tem um responsável, a Lia não consegue pegar, pois aquela tarefa já tem um responsável.
- No MVP, o sistema sabe quem é a pessoa pela lista de nomes escolhida ao abrir o quadro (login fica para depois).
- Só dá para pegar tarefa sem dono da coluna "A fazer".
- No MVP não dá para tirar o responsável de uma tarefa. Mais pra frente, só o tech lead poderá trocar os devs de tarefa.

## Fora do escopo (o que NÃO fazer agora)
- Criar tarefa
- Fazer PR (revisão de código)
- Login
- Mover a tarefa entre colunas
- Devolver uma tarefa que já pegou
- Filtrar só as tarefas da Lia

## Como saber que ficou pronto (critérios de aceite)
- **Dado** uma tarefa que o Pedro já pegou e uma que ninguém pegou, **quando** a Lia abre o quadro, **então** ela vê o nome "Pedro" na primeira e "sem dono" na segunda.
- **Dado** uma tarefa que já tem o Pedro como responsável, **quando** a Lia tenta pegar essa tarefa, **então** ela não consegue, pois aquela tarefa já tem um responsável.

## O que a IA perguntou (rodada 2)
52 perguntas (na rodada 1 foram ~150, sobre o sistema inteiro). Classificação de 3:
- Pergunta 1, como identificar quem clicou sem login: buraco real. Corrigido: lista de nomes ao abrir o quadro.
- Pergunta 22, pegar tarefa sem dono em qualquer coluna: buraco real. Corrigido: só da coluna "A fazer".
- Pergunta 16, "sem dono" ou "não atribuída": pergunta à toa. Qualquer texto resolve; fica "sem dono".

---

## Versão 1 (rodada 1 com a IA — guardada como evidência)

objetivo: transformar o problema em solução. o problema é falta de organizaocao dentro da labs!
contexto: a labs é uma empresa de software house que tem um cliente a renata que tem uma loja, porem ela passa as tarefas pro tech lead dentro do grupo do zap,porem o tech lead e os devs ficam sem organizacao entao as vezes dois devs resolvem o mesmo bug, e depois descobrem que o outro ja tinha feito, ou tarefas ficam dias pendentes pois sao esquecidas no meio da bagunca.
o que deve acontecer: a re passa as tarefas pro tech lead, ele vai la e joga a tarefa no a fazer, um dev pega a tarefa e se tora responsavel por ela, ele joga pra fazendo, ou em andamento. depois disso ele joga pra tabela de para revisao, o tech lead vai la e revisa o PS daquele dev, e so assim a tarefa fica pronto e colocada na tabela feito, ou concluido
regras e casos de erro: somente uma pessoa pode ficar resposavel por tal tarefa, somente o tech lead pode revisar aquele PR ou um dev de mais alto nivel, a re so passa as tarefas pro tech lead e ele cria as tarefas, nao a re! ela so eh leitora, entao nao aparece o botao de cirar tarefa pra ela!
fora do escopo: nao adivinhe nada para me dar o retorno dessa mensagem, liste suas duvidas e me pérgunte!

Resultado da rodada 1: a IA fez umas 150 perguntas, porque a spec descrevia o sistema inteiro, e não só a US-01.
