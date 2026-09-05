# Convenções comuns (obrigatórias em todos os 10 projectos)

Estas regras existem para o Grok Build gerar código consistente com o repositório
[BankingSystem](https://github.com/Claudio-Candido/BankingSystem), mas em **C puro**.

## Linguagem e compilação

- ISO C11 (`-std=c11`), avisos ligados: `-Wall -Wextra -Wpedantic`.
- Compilador: `gcc` (fallback `clang`).
- Build com **Makefile** (não CMake, não C++).
- Alvo principal: `make` → binário em `build/`.
- Alvo de testes: `make teste`.
- Sem bibliotecas externas. Apenas libc.
- Sem `new`/`class`/`namespace`/`iostream`. Isto é C, não C++.

## Português no código

- Identificadores, comentários e mensagens ao utilizador em **português**.
- Palavras reservadas da linguagem ficam em inglês (`int`, `return`, `struct`, `sizeof`, `FILE`, …).
- Identificadores C **não podem ter acentos**. Usar ASCII:
  - `registar_despesa`, `obter_saldo`, `validar_data`
  - `struct Medicamento`, `enum EstadoItem`
- Ficheiros: `despesa.c`, `despesa.h`, `interface_consola.c`.
- Constantes: `MAX_ITENS`, `CAMINHO_DADOS_PADRAO`.

## Arquitectura mínima (camadas)

```
ui/        menus e leitura do teclado
negocio/   regras (cálculos, validações de domínio)
dados/     persistência CSV ou binário
comum/     datas, validação, logging, utilitários
```

`main.c` só arranca o programa. Não misturar I/O com regras de negócio.

## Persistência

- Pasta `data/` criada em tempo de execução se não existir.
- Formato preferido: CSV com cabeçalho, UTF-8.
- Funções de escape/divisão de CSV próprias (vírgulas dentro de campos).
- Carregar tudo na arranque; gravar após cada mutação (ou no encerramento **e** após mutação — o utilizador não pode perder dados se fechar o programa).
- Caminho de dados configurável por argumento: `./programa [pasta_dados]`.

## Qualidade

- Validar toda a entrada (`fgets` + parse; nunca `scanf("%s")` sem limite).
- Tratar erros de `malloc`/`fopen`.
- Datas no formato `AAAA-MM-DD`.
- Valores monetários em **Kz (AOA)** com 2 casas, armazenados em `long` (centimos) para evitar erros de `float`.
- Testes em `tests/testes.c` com `assert` (sem framework).
- `README.md` + `docs/ARCHITECTURE.md` + `docs/GUIA_UTILIZADOR.md`.
- Pelo menos 3 imagens em `docs/imagens/`:
  1. `arquitetura.png` — diagrama das camadas
  2. `fluxo.png` — fluxo principal da tarefa do dia-a-dia
  3. `consola.png` — captura ou mock fiel do menu em terminal

## Imagens

Gerar PNGs simples (diagrama + mock de terminal). Se o ambiente não permitir captura real,
criar mocks em PNG com o aspecto de um terminal escuro e texto em português.

## Licença e segurança

- MIT.
- Sem palavras-passe reais, sem rede, sem dados sensíveis.
- Aviso no README: ferramenta de estudo, não produção.

## Estrutura-tipo de cada repositório

```
nome-do-projecto/
├── Makefile
├── README.md
├── LICENSE
├── include/
├── src/
├── tests/
├── docs/
│   ├── ARCHITECTURE.md
│   ├── GUIA_UTILIZADOR.md
│   └── imagens/
└── data/          # .gitkeep; ficheiros gerados em runtime
```
