# Spec visual — os cards do Quadro

## O que cada card mostra
## Como o responsável aparece (o nome)
## Como um card "sem dono" se diferencia de um com dono
## Como o título do card se destaca do resto
## O que acontece no celular (375 px)
## Regras que não podem quebrar (contraste, foco, cores das colunas que já existem)
## Fora do escopo (o que a IA NÃO deve mexer)

1-cada card mostra bem claro a tarefa que deve ser realizada a cor dela e quem é o responsavel embaixo no mesmo quadrante! 
2-o nome do responsavel fica embaixo to titulo da tarefa porem dentro da linha daquele quadro
3-um card sem dono fica inteiro vermelho e nao so a borda dele!
4-o titulo se destaca pelo contraste que vai existir entre a cor do quadro e a cor do titulo!
5-no celular ha responsividade e cada lista de cards ficam empilhados!
6-nao podem quebrar: as cores das colunas que ja existem, o contraste e responsividade para telas menores.
7-nao mexa no html, e nenhuma regra de negocio!

## Revisão do CSS da IA (20/10/2026)

### Comentários por seção da spec (as palavras do Edu)
1. aprovo, pois foi exatamente o que eu pedi
2. aprovado, pois foi como eu imaginei mesmo
3. aprovado, queria mesmo um diferencial claro de como ficaria um card com dono e um sem dono
4. aprovadíssimo, mudança básica, porém fundamental, gostei então aprovo!
5. certo, queria que os dispositivos médios como tablet não fossem esquecidos mesmo!
6. aprovado, não quebrou nenhuma regra
7. ela não fez pois teria que mexer no html e eu disse pra não mexer, ela respeitou! ótimo, IA respeitando as decisões sempre é fundamental

### Decisões sobre as regras que a IA escreveu
- **2 colunas no tablet (`@media` 1000 px): ACEITO**, porque no tablet ficaria tudo pequeno e minúsculo. A IA propôs sem estar na spec; a decisão passou a ser minha.
- **Regras `article:has(p)` e `article:has(p:first-of-type)` + variável `--cor-sem-dono` sem uso: RECUSO e apaguei.** Pegavam todos os cards e só repetiam o fundo branco: código morto que parecia atender o item 3 da spec. CSS não lê o texto "sem dono".
- **Contraste: AJUSTO.** O título "Revisão" com texto branco ficou abaixo de 4,5 (fui eu que troquei o texto para branco): escureci o amarelo para `#8a6a00`. O card sem dono com `#d64545` dava ~4,4: escureci para `#a50000` (~8:1).
- **Card sem dono inteiro vermelho: EXCEÇÃO NO HTML AUTORIZADA** (classe `sem-dono` nos 2 cards), porque o item 3 da spec só é possível marcando os cards no HTML.

### O que aprendi revisando
O item 3 parecia atendido e não estava; o item 6 parecia ok e o contraste estava quebrado. A conferência só vale olhando a tela e a régua, não só lendo o que a IA diz.

