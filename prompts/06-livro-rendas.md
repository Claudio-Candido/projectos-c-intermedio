# 06 — Livro de Rendas

**Repositório:** `Claudio-Candido/livro-rendas`  
**Inspiração:** o caderno do senhorio ou do inquilino onde se apontam as mensalidades, o recibo e o que ainda falta.

## Competências C

Estado de um contrato ao longo dos meses, geração de competência (AAAA-MM), recibo em ficheiro de texto, saldo em dívida.

## Prompt para o Grok Build

```
Cria um projecto completo em C11 chamado livro-rendas e publica-o no GitHub
em Claudio-Candido/livro-rendas (público, MIT).

OBJECTIVO
Registar um ou mais contratos de arrendamento (ou prestações fixas mensais)
e ir lançando pagamentos. Serve tanto ao senhorio como ao inquilino.

REGRAS DE CÓDIGO
- ISO C11, gcc, Makefile, -Wall -Wextra -Wpedantic.
- Português nos identificadores/UI; keywords em inglês; sem acentos nos nomes C.
- Sem C++ nem libs externas. Camadas comum / dados / negocio / ui.
- Dinheiro em long (centimos), Kz. CSV contratos.csv e pagamentos.csv.
- Testes: saldo em dívida, recibo, mês em atraso.

FUNCIONALIDADES
1. Criar contrato: id, imovel (texto), locador, locatario, valor_mensal,
   dia_vencimento (1–28), data_inicio, data_fim opcional, ativo.
2. Gerar automaticamente as competências (meses) desde data_inicio até ao
   mês corrente, se ainda não existirem.
3. Lançar pagamento: contrato, competencia AAAA-MM, valor, data, metodo
   (numerario, transferencia, outro). Aceitar pagamento parcial.
4. Consultar extrato do contrato: cada mês, valor devido, pago, estado
   (pago, parcial, em_atraso, a_vencer).
5. Lista de atrasados (vencimento já passou e saldo > 0).
6. Emitir recibo texto em data/recibo_<contrato>_<competencia>.txt
   com número sequencial de recibo.
7. Encerrar contrato (deixa de gerar meses novos).

Sem juros compostos. Se quiseres multa fixa por atraso, usa uma constante
documentada (ex.: 5% uma vez), facilmente desligável.

DOCUMENTAÇÃO
README.md (demo, sem valor jurídico), docs/ARCHITECTURE.md,
docs/GUIA_UTILIZADOR.md, docs/imagens/arquitetura.png, fluxo.png, consola.png.
LICENSE MIT.

Implementa, testa, commit e push.
```
