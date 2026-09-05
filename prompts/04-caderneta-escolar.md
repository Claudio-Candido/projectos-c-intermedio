# 04 — Caderneta Escolar

**Repositório:** `Claudio-Candido/caderneta-escolar`  
**Inspiração:** a caderneta que os encarregados de educação levam à reunião de pais — notas, médias e faltas.

## Competências C

Matriz lógica aluno × disciplina, médias ponderadas, situação final (aprovado / recuperação / reprovado), exportação de boletim.

## Prompt para o Grok Build

```
Cria um projecto completo em C11 chamado caderneta-escolar e publica-o no
GitHub em Claudio-Candido/caderneta-escolar (público, MIT).

OBJECTIVO
Gerir uma turma pequena (máx. 40 alunos, máx. 12 disciplinas): lançar notas
por trimestre, calcular médias e emitir um boletim em texto.

REGRAS DE CÓDIGO
- ISO C11, gcc, Makefile, -Wall -Wextra -Wpedantic.
- Português nos identificadores/UI; keywords em inglês; sem acentos nos nomes C.
- Sem C++ nem libs externas. Camadas comum / dados / negocio / ui.
- Notas em inteiros 0–200 (décimos: 145 = 14,5) para evitar float nas comparações.
  Mostrar sempre com uma casa decimal.
- CSV alunos.csv, disciplinas.csv, notas.csv, faltas.csv.
- Testes: média ponderada, arredondamento, situação final, limites da turma.

FUNCIONALIDADES
1. Registar disciplina (nome, peso).
2. Registar aluno (numero, nome, encarregado, telefone).
3. Lançar nota: aluno, disciplina, trimestre (1/2/3), valor.
4. Lançar falta (data, justificada ou não).
5. Consultar boletim de um aluno: notas por disciplina e trimestre,
   média da disciplina, média global, nº faltas.
6. Pauta da turma numa disciplina.
7. Situação provisória no 3.º trimestre:
   media >= 10,0 aprovado; 8,0–9,9 recuperacao; < 8,0 reprovado.
   (Documentar a regra no README; é uma convenção pedagógica de exemplo,
   não o regulamento oficial de Angola.)
8. Exportar boletim para data/boletim_<numero>.txt.

MENU em português.

DOCUMENTAÇÃO
README.md, docs/ARCHITECTURE.md, docs/GUIA_UTILIZADOR.md,
docs/imagens/arquitetura.png, fluxo.png, consola.png. LICENSE MIT.

Implementa, testa, commit e push.
```
