# 05 — Armário de Medicamentos

**Repositório:** `Claudio-Candido/armario-medicamentos`  
**Inspiração:** a caixa de medicamentos em casa — o que falta, o que caducou, o que se toma de manhã e à noite.

## Competências C

Datas (diferença em dias sem libc extra além de `time.h`), ordenação FEFO (primeiro a caducar sai primeiro), alertas, estruturas com validade.

## Prompt para o Grok Build

```
Cria um projecto completo em C11 chamado armario-medicamentos e publica-o no
GitHub em Claudio-Candido/armario-medicamentos (público, MIT).

OBJECTIVO
Controlar o stock caseiro de medicamentos: validade, quantidade e lembretes
de toma. NÃO é um sistema clínico. Incluir aviso grande no README:
não substitui médico nem bula.

REGRAS DE CÓDIGO
- ISO C11, gcc, Makefile, -Wall -Wextra -Wpedantic.
- Português nos identificadores/UI; keywords em inglês; sem acentos nos nomes C.
- Sem C++ nem libs externas. Camadas comum / dados / negocio / ui.
- Datas AAAA-MM-DD. Funções proprias: data_validar, data_hoje, data_diff_dias.
- CSV lotes.csv e tomas.csv. Testes de datas e de FEFO.

FUNCIONALIDADES
1. Registar medicamento/lote: nome, dosagem (texto), quantidade (comprimidos
   ou ml), validade, local (armario, frigorifico), nota.
2. Dar baixa (toma ou desperdício) escolhendo sempre o lote que caduca primeiro
   (FEFO). Recusar se quantidade insuficiente.
3. Painel do dia: lotes caducados, a caducar em 30 dias, stock a zero.
4. Lista FEFO completa.
5. Agenda simples de tomas: medicamento, hora HH:MM, dose em unidades.
   Ao arrancar, mostrar as tomas do dia.
6. Registar que a toma foi feita (data+hora).
7. Remover lote caducado (com confirmação).

DOCUMENTAÇÃO
README.md com aviso de saúde, docs/ARCHITECTURE.md, docs/GUIA_UTILIZADOR.md,
docs/imagens/arquitetura.png, fluxo.png, consola.png. LICENSE MIT.

Implementa, testa, commit e push.
```
