# 08 — Câmbio do Kwanza

**Repositório:** `Claudio-Candido/cambio-kwanza`  
**Inspiração:** a pergunta diária «a quanto está o dólar hoje?» e o papel onde se aponta a taxa da praça / do banco.

## Competências C

Histórico temporal, conversão bidireccional, escolha da taxa mais recente <= data pedida, média móvel simples de 7 dias.

## Prompt para o Grok Build

```
Cria um projecto completo em C11 chamado cambio-kwanza e publica-o no GitHub
em Claudio-Candido/cambio-kwanza (público, MIT).

OBJECTIVO
Registar manualmente as taxas do dia (não há API) e converter entre Kz, USD
e EUR. Útil para quem compra no informal ou compara com o banco.

REGRAS DE CÓDIGO
- ISO C11, gcc, Makefile, -Wall -Wextra -Wpedantic.
- Português nos identificadores/UI; keywords em inglês; sem acentos nos nomes C.
- Sem C++ nem rede nem libs externas. Camadas comum / dados / negocio / ui.
- Taxas e montantes: Kz em long (centimos). USD/EUR em long (cêntimos).
  Taxa armazenada como inteiro: kz_por_100_unidades_estrangeiras
  (ex.: 1 USD = 850,50 Kz → 85050). Documentar a escala.
- CSV taxas.csv (data, par, valor, fonte: banco/praca/outro).
- Testes de conversão, escolha da taxa na data, média 7 dias.

FUNCIONALIDADES
1. Lançar taxa do dia para USD/AOA e EUR/AOA (compra e venda, opcionalmente
   só uma taxa média se o utilizador não distinguir).
2. Converter: montante + moeda origem + moeda destino + data
   (usa a última taxa com data <= pedida).
3. Histórico de um par, N últimos dias.
4. Variação percentual face ao dia anterior e face a 7 dias.
5. Média simples dos últimos 7 registos.
6. Exportar historico_USD.csv filtrado.

Ao arrancar, mostrar a última taxa conhecida de USD e EUR.

Aviso no README: taxas manuais, sem valor oficial, não é serviço financeiro.

DOCUMENTAÇÃO
README.md, docs/ARCHITECTURE.md, docs/GUIA_UTILIZADOR.md,
docs/imagens/arquitetura.png, fluxo.png, consola.png. LICENSE MIT.

Implementa, testa, commit e push.
```
