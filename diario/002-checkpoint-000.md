Github é uma plataforma aonde vc guarda seus codigos de um jeito muito seguro, Git é um programa que é um caminho pra colocar todos os seus codigos, mudancas nos arquivos dentro do github!

git add consegue colocar toda a pasta? e o commit tbm ne! nao sei entao! 

eu diria que o node nao foi reconhecido

porque button é reconhecido por tab e enter, ja caixinha colorida nao!

nao sei de vdd



O Quadro vai ser usado por 6 pessoas ao mesmo tempo, o dia inteiro.
Se duas pessoas moverem o mesmo card no mesmo segundo, qual movimento vale?
Se o servidor cair às 18h de uma sexta, quem percebe, e como?
Como você atualiza o sistema sem derrubar quem está usando?



Revisão do index.html (estado atual, commit mais recente), como num PR:

Resumo: é uma página mínima, válida e acessível no básico (lang, charset, viewport, <button> de verdade). Não tem nada quebrado. Os pontos abaixo são de estrutura e de coisas que vão dar problema quando o Quadro crescer.

🟠 Vai dar problema logo

O <button> não tem type (linha 13). Sem type="button", o padrão é submit. Hoje não acontece nada, mas na 001.4 o botão vai ficar dentro de um <form>. Aí cada clique vai enviar o formulário e recarregar a página, e os cards vão sumir sem erro nenhum no console.
O título “A fazer” não está ligado a nada (linha 14). Ele é o nome de uma coluna, mas a coluna não existe na estrutura. Quando os cards chegarem, não vai haver um elemento que agrupe “esta coluna e os cards dela”. Isso dificulta o CSS (grid de colunas) e o leitor de tela.

🟡 Estrutura e acessibilidade
3. Falta marcar as regiões da página. Tudo está solto no <body>. Não há nada separando o cabeçalho (título, descrição, botão de ação) do conteúdo principal (o quadro). Quem usa leitor de tela navega pulando entre essas regiões, e hoje não existe nenhuma.
4. Maiúsculas sem padrão: “Quadro” (primeira maiúscula), “a fazer” (tudo minúsculo), “NOVA TAREFA” (tudo maiúsculo). Escolha uma regra. Se a ideia é que o botão pareça todo em caixa alta, isso é decisão visual e costuma ser feita no CSS, não escrita no texto.
5. O nome da coisa está trocado. O produto chama a unidade de trabalho de card (glossário da Parte 15), e o botão diz “tarefa”. Isso vem do desafio da M8, então foi intencional. Mas, numa base de código, o mesmo conceito com dois nomes vira confusão no código e no banco. Vale decidir qual palavra o produto usa e manter só ela.

⚪ Detalhes
6. 4 linhas em branco antes do </body> (linhas 15–18). Viram ruído no próximo diff.
7. style.css vazio está sendo carregado e foi commitado sem conteúdo. Não é erro, porque vai ser usado no Ato 1, mas um arquivo vazio no histórico pede uma mensagem de commit que explique por que ele existe.
8. lang="pt-br" funciona, porque o atributo não diferencia maiúsculas. A convenção mais comum é pt-BR. É só consistência.


nao sabia do type do button, definira varias divs, deixaria tudo padronizado
1-aceito, acho que seria uma melhor organizacao no futuro
2-recuso, foi proposital para o testo/começo
3-aceito com ressalvas, divs sao extremamente importantes, porém para um primeiro momento, nao sera aceita
4-aceito, tenho que manter uma padronizacao das coisas 
5-recuso, proposital
6-aceito, achei que nao teria problema e pra mim é melhor para a organizacao e leitura
7-concordo, porem no futuro ele sera usado, por isso ja deixei ele ali
8-ok