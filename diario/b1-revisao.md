# B1 · A Revisão (20/10/2026)

Boss de revisão, sem IA. Código revisado: `b1-revisao/coluna.html` e `b1-revisao/coluna.css`.
Ferramentas: validador W3C, Tab no teclado, DevTools (modo celular) e a régua de contraste.

> Registro transcrito pelo Claude a partir das respostas do Edu no chat. Os achados são do Edu.
> A coluna "Como corrigir" foi preenchida pelo Edu.

| # | Onde | Problema | Evidência | Como corrigir |
|:-:|---|---|---|---|
| 1 | `coluna.html`, títulos dos cards | O h4 pula o nível: vai do h2 direto para o h4 | Validador W3C | colocar o Hs sempre em ordem |
| 2 | `coluna.html` | Não tem h1 na página | Validador W3C | colocar um h1 |
| 3 | `coluna.css`, `button:focus` | Quando aperto Tab, o botão não fica marcado | `button:focus { outline: none; }` | colocar um outline diferente de none como 3px solid var |
| 4 | Textos dentro do quadro ("Corrigir total do pedido...", responsável) | Texto branco com fundo vermelho: reprova no contraste | Régua: 3.63, abaixo do mínimo de 4.5 | deixar um contraste mais forte mais alto ou agual que 4,5 |
| 5 | `coluna.css`, `.coluna` | Sem responsividade: vaza no celular | `width: 520px` | Já corrigi na mão: troquei para 100%  colocar em 100%
| 6 | `coluna.html`, `section` | O `aria-labelledby` aponta para `col-a-fazer`, mas o id é `coluna-a-fazer` | Comparando letra por letra | sempre colocar exatamente igual um ao outro |

