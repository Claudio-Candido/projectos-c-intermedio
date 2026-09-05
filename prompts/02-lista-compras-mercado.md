# 02 — Lista de Compras do Mercado

**Repositório:** `Claudio-Candido/lista-compras-mercado`  
**Inspiração:** o papel que se leva ao mercado ou à cantina — quantidade, preço estimado, o que já foi posto no saco.

## Competências C

Pesquisa linear e por nome (case-insensitive), ordenação (`qsort` com comparadores), `enum EstadoItem`, estimativa vs. gasto real.

## Prompt para o Grok Build

```
Cria um projecto completo em C11 chamado lista-compras-mercado e publica-o no
GitHub em Claudio-Candido/lista-compras-mercado (público, MIT).

OBJECTIVO
Gerir a lista de compras da casa: o que falta, quanto levar, quanto se pensa
gastar e quanto se gastou de facto no mercado.

REGRAS DE CÓDIGO
- ISO C11, gcc, Makefile, -Wall -Wextra -Wpedantic.
- Identificadores/comentários/mensagens em português; keywords em inglês;
  identificadores sem acentos.
- Sem C++ nem libs externas. Camadas comum / dados / negocio / ui.
- Dinheiro em long (centimos), Kz. Persistência CSV em data/.
- fgets + validação. Testes com assert.

FUNCIONALIDADES
1. Criar lista nomeada (ex.: "Sabado Roque Santeiro" ou "Cantina do bairro").
2. Acrescentar item: nome, unidade (kg, L, un, saco), quantidade, preco_estimado,
   seccao (talho, peixe, verdura, cereais, limpeza, outros).
3. Marcar item como comprado, indicando preco_real e quantidade_real.
4. Desmarcar / editar / remover item.
5. Ordenar lista por secção, por nome ou por por comprar primeiro.
6. Pesquisar item por substring.
7. Resumo: nº itens, nº por comprar, total estimado, total real, diferença.
8. Duplicar lista (útil para a semana seguinte).
9. Gravar/carregar automaticamente.

MENU numerado em português.

DOCUMENTAÇÃO
README.md, docs/ARCHITECTURE.md, docs/GUIA_UTILIZADOR.md,
docs/imagens/arquitetura.png, fluxo.png, consola.png.
LICENSE MIT. data/.gitkeep.

Implementa, testa (make && make teste), commit e push.
```
