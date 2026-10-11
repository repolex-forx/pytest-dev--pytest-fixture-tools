# Repolex Knowledge Graph of pytest-dev/pytest-fixture-tools

RDF knowledge graph data for [pytest-dev/pytest-fixture-tools](https://github.com/pytest-dev/pytest-fixture-tools), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [rlex](https://github.com/repolex-ai/rlex) query tool:

```bash
cargo install --git https://github.com/repolex-ai/rlex
```

Verify the install:

```bash
rlex --help
```

**rlex is designed to be used primarily by LLMs in a terminal.** Start up your favorite AI assistant and ask it to use rlex. It handles the SPARQL — you just ask questions in plain English.

To load this repo's data:

```bash
rlex download pytest-dev/pytest-fixture-tools
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── f7ac6315451d0c537454648e04a8dd13fabee989
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── f7ac6315451d0c537454648e04a8dd13fabee989
│           └── chunk-001.nq.gz
├── blob
│   ├── 043363fb946eca422bcc012f6d25a255b1b5d3a7.nq.gz
│   ├── 118a8c04da4d34e6ca196edcb502bd34fa48d454.nq.gz
│   ├── 121f1b32ea9baae616fdd345a1adf87fddff2e26.nq.gz
│   ├── 241086240fc7c92a08788d5ddaab43bf39604ce9.nq.gz
│   ├── 34d12fa61d1465993cea5b6f53409e86d49b91b5.nq.gz
│   ├── 42c2780292b6ef968300c62e4876e7e39149e226.nq.gz
│   ├── 6acc198115acd57b185d8f77153cf78c836fa409.nq.gz
│   ├── 73fc2f34a73cba7d4d865bad39f4aeedfaa8d2c1.nq.gz
│   ├── 7d1de486cfdd693d02320c5a40d9c9a022f0b6a1.nq.gz
│   ├── 8ba6e0bd1628758db130339322b05be0a67306d2.nq.gz
│   ├── b5abb13c72b802113a82d280f8c1a73e012e7fd3.nq.gz
│   ├── ca3943d8b35843c66f9beb779aa52b48c5f15101.nq.gz
│   ├── d36f0df5f15b11beee22b7477d553ea8a020c73a.nq.gz
│   ├── d91a1d8dc2771cd42ee4d2dba2584d3249ce4e98.nq.gz
│   └── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── f7ac6315451d0c537454648e04a8dd13fabee989.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 23 files
```

| Directory | What it contains |
|-----------|-----------------|
| `blob/` | Per-file AST graphs, content-addressed by git blob SHA. Each file in the source repo gets its own graph. |
| `aggregate/ast/` | Combined AST graph per parsed commit. Merges all blob graphs for a snapshot of the entire codebase at that point. |
| `aggregate/lsp/` | Language Server Protocol enrichment: resolved symbols, definitions, references, and type information. |
| `aggregate/dataflow/` | Interprocedural data flow edges between functions and modules. |
| `aggregate/repolex/` | Combined graph (AST + LSP + dataflow) per commit. |
| `commit/` | Git commit metadata (author, date, message, parent links). |
| `branch/` | Branch metadata. |
| `tag/` | Tag metadata. |
| `filetree/` | File tree snapshots per commit (which files existed and their blob SHAs). |
| `audit/` | Code architecture and graph audit reports per commit. |

## Source repository

[pytest-dev/pytest-fixture-tools](https://github.com/pytest-dev/pytest-fixture-tools)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
