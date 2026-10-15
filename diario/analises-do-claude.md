# Análises do Claude

O que o Claude (mentor da campanha) observou em cada SUBOP: o que ficou firme, o que ainda
está frágil e o que revisar. É a visão de fora. A visão de dentro é o meu diário.

---

## SUBOP 001.0 — O Laboratório (06/10 e 13/10) · 360 XP

**Firme**
- Terminal: `pwd`, `ls`, `cd`, `mkdir`, `Remove-Item -Recurse`.
- Git no dia a dia: `init`, `add`, `commit -m`, `log`, `push`, `remote`, `branch -M main`.
- Identidade do Git configurada só no repositório (o PC é do primo), com e-mail noreply do GitHub.
- Primeira tela publicada e primeira revisão de IA feita com aceito/recuso, sem aceitar tudo no automático.

**Frágil**
- O que é o **PATH**: chegou em "não foi encontrado", mas não em "onde o Windows procura". Revisão espaçada.
- Diferença **commit × push**: confundiu duas vezes antes de firmar. O push escapou em 2 fins de sessão (`ahead 1`).

**Hábito bom** — "usei para realmente aprender e não só para fingir que acertei" (mensagem de commit do checkpoint).

---

## SUBOP 001.1 — O Briefing (13/10 e 14/10) · +275 XP (com bônus)

**Firme**
- Problema × requisito, e requisito sem tecnologia e verificável.
- User story completa: "como / quero / para" + critérios Dado / quando / então com caso de erro.
- Achou os **3 furos plantados** da Parte 15 sozinho (RN-09 com #12 em vários projetos, RN-03 × RN-07, "arquivar" sem definição).
- Spec para IA: de ~150 perguntas (versão 1, o sistema inteiro) para 52 (versão 2, só a US-01). Decidiu sozinho os 2 buracos reais que a IA achou (identificar quem clicou sem login; só pegar tarefa de "A fazer").

**Frágil**
- Separar **"para" × "então"**: colocava o benefício no critério. Levou várias rodadas até destravar.
- Tendência a escrever **o sistema inteiro** quando o pedido é **uma parte** (spec v1, objetivo genérico). Treinar o recorte.
- Pede para o Claude escrever partes que são o exercício (spec). Quando o Claude devolveu com perguntas, ele fez — e fez bem.

**Hábito bom** — pergunta "e se...?" e "o que acontece quando...?" (foi assim que achou os furos).

---

## SUBOP 001.2 — A Primeira Tela (14/10 e 15/10) · em andamento

**Firme**
- Regiões semânticas (`header`, `main`, `footer`) e por que não `div`.
- `section` + `aria-labelledby` ligando ao `id` do `h2`.
- `value` técnico sem acento e texto da tela com acento (fez sozinho no filtro).
- `name` × `id` × texto do label; `required` e `maxlength` (RN-02) no formulário.
- Código-fonte × DOM, aprendido pelo experimento do `</h3>`.
- Teste de acessibilidade real: ordem do Tab e Narrador (achou o "DEVs" lido como sigla).
- HTML válido no W3C sem nenhum erro.

**Frágil**
- **Por que `<ul>`/`<li>`** (quem percebe: quem usa leitor de tela) e **o que o `for` do label faz** (liga ao `id`; clique foca; leitor lê o nome). Precisou da resposta na prova. Revisão espaçada.
- **Padrão de escrita**: caixa alta misturada no HTML ("QUADRO", "DEVs", "+Novo Card"); dois jeitos de label (lado a lado × envolvendo). Regra: no HTML escreve normal; caixa alta é CSS.
- Atenção a detalhes do pedido: esqueceu o `<main>` na M1, fez 3 `<ul>` numa coluna na M3, nomes de coluna diferentes da Parte 15 (a sugestão do Copilot empurrou nomes errados — desligou o autocomplete).

**Hábito bom** — mensagens de commit melhoraram: passaram a dizer o porquê.

---

## Para revisar sem aviso (revisão espaçada)
- O que é o PATH
- Commit × push (e terminar sempre com `git status`)
- Por que `<ul>`/`<li>` e não `<div>`
- O que o `for` do `<label>` faz
