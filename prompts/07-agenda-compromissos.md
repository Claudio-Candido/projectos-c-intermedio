# 07 — Agenda de Compromissos

**Repositório:** `Claudio-Candido/agenda-compromissos`  
**Inspiração:** a agenda de papel / WhatsApp onde se mistura consulta no hospital, reunião, missa e aniversário.

## Competências C

Lista ligada ordenada por data+hora, inserção ordenada, recorrência semanal simples, lembretes «hoje» e «próximos 7 dias».

## Prompt para o Grok Build

```
Cria um projecto completo em C11 chamado agenda-compromissos e publica-o no
GitHub em Claudio-Candido/agenda-compromissos (público, MIT).

OBJECTIVO
Agenda de terminal para a vida pessoal: compromissos pontuais e semanais
(ex.: culto ao domingo, treino à quarta).

REGRAS DE CÓDIGO
- ISO C11, gcc, Makefile, -Wall -Wextra -Wpedantic.
- Português nos identificadores/UI; keywords em inglês; sem acentos nos nomes C.
- Sem C++ nem libs externas. Camadas comum / dados / negocio / ui.
- Compromissos em lista ligada (struct No), sempre ordenada por data e hora.
  Persistência CSV (a lista é reconstruída e reordenada no load).
- Datas AAAA-MM-DD, horas HH:MM. Testes de inserção ordenada e recorrência.

FUNCIONALIDADES
1. Criar compromisso: titulo, local, data, hora, duracao_min, categoria
   (saude, trabalho, familia, religiao, escola, outro), notas.
2. Compromisso semanal: dia_da_semana + hora; o programa materializa as
   próximas 8 ocorrências à consulta (não precisa de gerar anos inteiros).
3. Listar hoje, amanhã, próximos 7 dias, mês.
4. Pesquisar por texto.
5. Marcar como concluido / cancelado (não apaga o histórico).
6. Editar e apagar.
7. Ao arrancar, mostrar «hoje» e os 3 próximos.

MENU em português. Confirmar exclusões.

DOCUMENTAÇÃO
README.md, docs/ARCHITECTURE.md, docs/GUIA_UTILIZADOR.md,
docs/imagens/arquitetura.png, fluxo.png, consola.png. LICENSE MIT.

Implementa, testa, commit e push.
```
