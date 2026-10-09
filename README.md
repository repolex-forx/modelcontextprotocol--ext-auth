# Repolex Knowledge Graph of modelcontextprotocol/ext-auth

RDF knowledge graph data for [modelcontextprotocol/ext-auth](https://github.com/modelcontextprotocol/ext-auth), parsed by [repolex](https://repolex.ai).

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
rlex download modelcontextprotocol/ext-auth
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── fb374c7db2b34f18ca9183882e0beecdf661892b
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── fb374c7db2b34f18ca9183882e0beecdf661892b
│           └── chunk-001.nq.gz
├── blob
│   ├── 2278d60478cf6cb2ba7877d2e5d32e264b8d0ccd.nq.gz
│   ├── 22f1f0dc30ab41a0f8821d82e11b4d20f95bef9b.nq.gz
│   ├── 29aadea8534e08d2b51f875e805865778681da9e.nq.gz
│   ├── 50292420096eb98f07f3945dc30325fe8b17a2af.nq.gz
│   ├── 586ce278e9a3ff41dee9f3c47fceaf0202bc6ab1.nq.gz
│   ├── 640e9d994319b47c447baa85ec012321f0fdaea2.nq.gz
│   ├── 87feddf2c4dfcbae75e7aa4e25de54f835cff472.nq.gz
│   ├── 98bece0746bdf189ef13a6b556b8daf979045105.nq.gz
│   ├── a336e27a0ccb173d97cfdc091ebe324251b8e5bb.nq.gz
│   ├── b5031a009ced607665b1359a145d074e2c41220a.nq.gz
│   └── ff125234dbec15ea5fb470e256c6a3cd3b9bbdd1.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── fb374c7db2b34f18ca9183882e0beecdf661892b.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 19 files
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

[modelcontextprotocol/ext-auth](https://github.com/modelcontextprotocol/ext-auth)

---
*Parsed on 2026-10-09 by [repolex](https://repolex.ai)*
