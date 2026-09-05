# 10 projectos C (nível intermédio) — tarefas do dia-a-dia

Catálogo de **prompts prontos para o Grok Build**. Cada projecto modela uma tarefa
real do quotidiano, em **C11**, com identificadores e mensagens em português
(excepto palavras reservadas da linguagem).

Conta GitHub: [Claudio-Candido](https://github.com/Claudio-Candido).
Estilo de documentação alinhado com [BankingSystem](https://github.com/Claudio-Candido/BankingSystem)
(`README` + `docs/` + imagens em `docs/imagens/`).

## Como usar com o Grok Build

1. Abre o ficheiro `prompts/NN-nome.md`.
2. Copia o bloco **«Prompt para o Grok Build»** na íntegra.
3. Pede para criar o repositório `Claudio-Candido/<nome>` (público, MIT).
4. Confirma: `make && make teste` e README com as 3 imagens.

Regras partilhadas: [CONVENCOES.md](CONVENCOES.md).

## Os 10 projectos

| # | Repositório sugerido | Tarefa do dia-a-dia | Conceitos C em destaque |
|---|---|---|---|
| 01 | `caderno-despesas` | Anotar gastos do mês e ver se o orçamento chega | `struct`, CSV, agregação, dinheiro em centimos |
| 02 | `lista-compras-mercado` | Lista do mercado com quantidades e total | arrays, pesquisa, ordenação, estados |
| 03 | `caixa-quitanda` | Vendas do quiosque / zunga no fim do dia | stock, caixa, tickets de venda |
| 04 | `caderneta-escolar` | Notas, médias e faltas dos filhos / alunos | tabelas 2D, médias ponderadas |
| 05 | `armario-medicamentos` | Controlar comprimidos e validade em casa | datas, alertas, FEFO |
| 06 | `livro-rendas` | Recibos de aluguer e prestações em atraso | contratos, saldo em dívida |
| 07 | `agenda-compromissos` | Consultas, missa, trabalho, visitas | lista ligada, ordenação por data/hora |
| 08 | `cambio-kwanza` | Converter Kz ↔ USD/EUR e guardar o câmbio do dia | histórico, interpolação simples |
| 09 | `conta-luz-agua` | Estimar factura a partir das leituras do contador | consumo, escalões, gráfico ASCII |
| 10 | `despensa-casa` | O que há na despensa e o que está a acabar | inventário, ponto de encomenda |

Não repetem o sistema bancário já existente. São todos de consola, sem rede e sem GUI.

## Ordem recomendada

`01 → 02 → 04 → 09 → 08 → 07 → 05 → 06 → 10 → 03`

Sobe a complexidade de persistência e de regras de negócio.

## Premissas

- Ambiente POSIX (Linux). `mkdir` via `mkdir()` / fallback documentado.
- Texto UTF-8 no terminal; identificadores sem acentos.
- Moeda: Kwanza angolano (AOA), símbolo `Kz`.
- Nível: intermédio — vários `.c`/`.h`, ficheiros, ponteiros, testes. Não é «Hello World».
