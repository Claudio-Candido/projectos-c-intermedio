# 09 — Conta da Luz e da Água

**Repositório:** `Claudio-Candido/conta-luz-agua`  
**Inspiração:** apontar a leitura do contador quando passa o leitor, para não ser surpreendido pela factura.

## Competências C

Leituras monótonas (não podem descer), consumo = leitura_actual - anterior, escalões por blocos, gráfico de barras ASCII.

## Prompt para o Grok Build

```
Cria um projecto completo em C11 chamado conta-luz-agua e publica-o no GitHub
em Claudio-Candido/conta-luz-agua (público, MIT).

OBJECTIVO
Guardar leituras dos contadores de electricidade (kWh) e água (m3), estimar
o valor da factura com uma tabela de escalões CONFIGURÁVEL (não fingir que
é a tarifa oficial da ENDE/EPAL — o utilizador edita os escalões).

REGRAS DE CÓDIGO
- ISO C11, gcc, Makefile, -Wall -Wextra -Wpedantic.
- Português nos identificadores/UI; keywords em inglês; sem acentos nos nomes C.
- Sem C++ nem libs externas. Camadas comum / dados / negocio / ui.
- Leituras em long (kWh inteiros; m3 em litros para evitar float).
- Dinheiro em long (centimos), Kz.
- CSV contadores.csv, leituras.csv, escaloes.csv.
- Testes: consumo, rejeição de leitura menor, cálculo por escalões.

FUNCIONALIDADES
1. Registar contador: nome ("luz casa", "agua quintal"), tipo (luz/agua),
   unidade, leitura_inicial.
2. Lançar leitura (data, valor). Recusar se for menor que a anterior
   (excepto se o utilizador confirmar «substituição de contador»).
3. Consumo do período e estimativa em Kz segundo escalões:
   bloco 1 até X unidades a preço A, bloco 2 até Y a preço B, resto a C.
   Taxa fixa mensal configurável.
4. Comparar com o período anterior (percentagem).
5. Gráfico ASCII dos últimos 12 consumos.
6. Editar tabela de escalões.
7. Exportar estimativa data/estimativa_<contador>_<periodo>.txt.

Aviso no README: estimativa pedagógica, não factura oficial.

DOCUMENTAÇÃO
README.md, docs/ARCHITECTURE.md, docs/GUIA_UTILIZADOR.md,
docs/imagens/arquitetura.png, fluxo.png, consola.png. LICENSE MIT.

Implementa, testa, commit e push.
```
