# 10 — Despensa de Casa

**Repositório:** `Claudio-Candido/despensa-casa`  
**Inspiração:** abrir o armário e não saber se ainda há óleo, arroz ou sabão — e só descobrir no mercado.

## Competências C

Inventário com ponto de encomenda, movimentos de entrada/saída, lista automática «o que comprar», pesquisa, validade de perecíveis.

## Prompt para o Grok Build

```
Cria um projecto completo em C11 chamado despensa-casa e publica-o no GitHub
em Claudio-Candido/despensa-casa (público, MIT).

OBJECTIVO
Inventário da despensa e do armário de limpeza. Dá baixa quando se usa,
entrada quando se chega do mercado, e gera a lista do que está no mínimo.

REGRAS DE CÓDIGO
- ISO C11, gcc, Makefile, -Wall -Wextra -Wpedantic.
- Português nos identificadores/UI; keywords em inglês; sem acentos nos nomes C.
- Sem C++ nem libs externas. Camadas comum / dados / negocio / ui.
- Quantidades em milésimas da unidade (1000 = 1 kg) para evitar float.
- Dinheiro opcional em long (centimos) no custo médio ponderado simples.
- CSV itens.csv e movimentos.csv. Testes: ponto de encomenda, baixa, custo médio.

FUNCIONALIDADES
1. Cadastrar item: nome, categoria (grao, oleo, limpeza, higiene, enlatado,
   outro), unidade, stock, stock_minimo, validade_opcional, local (despensa,
   frigorifico, casa_banho).
2. Entrada (veio do mercado): quantidade, preco_total opcional → actualiza
   custo médio.
3. Saída (usou-se em casa): quantidade; recusar se não houver stock.
4. Ajuste de inventário (contagem real).
5. Lista «a comprar»: stock <= minimo, com quantidade sugerida
   (minimo * 2 - stock, no mínimo 1 unidade).
6. Alertas de validade a 15 dias.
7. Pesquisa e filtro por categoria / local.
8. Exportar lista de compras para data/para_comprar_AAAA-MM-DD.txt.

Pode integrar conceptualmente com o projecto 02 (lista de compras), mas
deve funcionar sozinho.

DOCUMENTAÇÃO
README.md, docs/ARCHITECTURE.md, docs/GUIA_UTILIZADOR.md,
docs/imagens/arquitetura.png, fluxo.png, consola.png. LICENSE MIT.

Implementa, testa, commit e push.
```
