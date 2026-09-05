# 03 — Caixa da Quitanda

**Repositório:** `Claudio-Candido/caixa-quitanda`  
**Inspiração:** o caderno da dona da quitanda / quiosque: o que entrou, o que saiu, o dinheiro da gaveta no fecho do dia.

## Competências C

Dois ficheiros CSV (produtos + movimentos), decremento de stock, cálculo de troco, relatório de fecho, ids sequenciais.

## Prompt para o Grok Build

```
Cria um projecto completo em C11 chamado caixa-quitanda e publica-o no GitHub
em Claudio-Candido/caixa-quitanda (público, MIT).

OBJECTIVO
Simular a caixa e o stock de uma quitanda ou quiosque de bairro. Não é um
POS real — é um exercício de persistência e regras de stock.

REGRAS DE CÓDIGO
- ISO C11, gcc, Makefile, -Wall -Wextra -Wpedantic.
- Português nos identificadores/comentários/UI; keywords em inglês; sem acentos
  nos nomes C.
- Sem C++ nem libs externas. Camadas comum / dados / negocio / ui.
- Dinheiro em long (centimos), Kz. Stock em inteiros (unidades) ou centésimos
  de kg quando a unidade for kg (documentar a escolha e ser consistente).
- CSV produtos.csv e movimentos.csv. Testes com assert.

FUNCIONALIDADES
1. Cadastrar produto: codigo, nome, unidade, preco_venda, stock, stock_minimo.
2. Entrada de stock (compra ao fornecedor) com custo opcional.
3. Venda: um ou mais itens, quantidade, calcula total, recebe valor_dado,
   devolve troco. Recusa se stock insuficiente.
4. Cancelar última venda do dia (estorno que devolve stock) — só a última,
   para manter a regra simples e testável.
5. Consultar stock; alertar produtos abaixo do mínimo.
6. Abrir caixa do dia (fundo inicial) e fechar caixa:
   fundo + vendas - estornos = esperado na gaveta.
   Pedir contagem real e mostrar quebra/sobra.
7. Relatório do dia em data/fecho_AAAA-MM-DD.txt.

Sem autenticação. Um único operador.

DOCUMENTAÇÃO
README.md (aviso: demo de estudo), docs/ARCHITECTURE.md,
docs/GUIA_UTILIZADOR.md (fluxo: cadastrar 3 produtos → vender → fechar caixa),
docs/imagens/arquitetura.png, fluxo.png, consola.png.
LICENSE MIT.

Implementa, testa, commit e push.
```
