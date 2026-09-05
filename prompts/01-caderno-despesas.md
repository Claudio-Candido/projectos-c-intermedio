# 01 — Caderno de Despesas do Mês

**Repositório:** `Claudio-Candido/caderno-despesas`  
**Inspiração:** o caderno (ou as notas no telemóvel) onde se aponta o pão, o candongueiro, o gás e o mercado, para saber se o salário ainda chega.

## Competências C

`struct Despesa`, arrays dinâmicos (`realloc`), CSV, categorias com `enum`, agregação por mês e por categoria, dinheiro em `long` (centimos).

## Prompt para o Grok Build

```
Cria um projecto completo em C11 chamado caderno-despesas e publica-o no GitHub
em Claudio-Candido/caderno-despesas (público, licença MIT).

OBJECTIVO
Programa de terminal que substitui o caderno de gastos do mês. O utilizador
regista cada despesa (data, categoria, descrição, valor em Kz), consulta totais
e compara com um tecto orçamental mensal.

REGRAS DE CÓDIGO
- ISO C11, gcc, Makefile, -Wall -Wextra -Wpedantic.
- Identificadores, comentários e mensagens em português. Palavras reservadas
  da linguagem em inglês. Identificadores SEM acentos (registar_despesa).
- Sem C++, sem bibliotecas externas.
- Camadas: comum / dados / negocio / ui. main.c só arranca.
- Dinheiro em long (centimos). Moeda Kz (AOA). Datas AAAA-MM-DD.
- Entrada com fgets + parse. Tratar malloc/fopen.
- Persistência CSV em data/ (criada se não existir). Argumento opcional com a
  pasta de dados.
- Testes com assert em tests/testes.c (parse monetário, CSV, totais, tecto).

FUNCIONALIDADES
1. Definir / alterar o orçamento do mês corrente (tecto em Kz).
2. Registar despesa: data, categoria, descrição, valor.
   Categorias (enum): alimentacao, transporte, casa, saude, educacao,
   comunicacao, lazer, outros.
3. Listar despesas do mês, com filtro por categoria.
4. Editar e apagar despesa por id.
5. Relatório do mês: total, total por categoria, percentagem de cada uma,
   restante até ao tecto, aviso se já ultrapassou (e por quanto).
6. Relatório de um mês anterior (AAAA-MM).
7. Exportar relatório texto para data/relatorio_AAAA-MM.txt.

MENU em português, claro, numerado. Confirmar exclusões.

DOCUMENTAÇÃO (obrigatória, estilo BankingSystem)
- README.md com tabela de funcionalidades, build, execução, estrutura.
- docs/ARCHITECTURE.md (camadas).
- docs/GUIA_UTILIZADOR.md (fluxo: definir tecto → registar 3 despesas → relatório).
- docs/imagens/arquitetura.png, fluxo.png, consola.png
  (mocks de diagrama e de terminal se não houver captura real).

Estrutura: Makefile, include/, src/, tests/, docs/imagens/, data/.gitkeep, LICENSE.

Implementa o código a funcionar, corre make e make teste, faz commit e push.
```
