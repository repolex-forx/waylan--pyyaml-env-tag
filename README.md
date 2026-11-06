# Repolex Knowledge Graph of waylan/pyyaml-env-tag

RDF knowledge graph data for [waylan/pyyaml-env-tag](https://github.com/waylan/pyyaml-env-tag), parsed by [repolex](https://repolex.ai).

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
rlex download waylan/pyyaml-env-tag
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 8f43568693ebd7fcad5c3b79ef6ce0072225914f
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 8f43568693ebd7fcad5c3b79ef6ce0072225914f
│           └── chunk-001.nq.gz
├── blob
│   ├── 0574063395c109295490fcef456a54fb9972a7d9.nq.gz
│   ├── 37a47314780365dbb1bc60916fe8ddc0d584fbf0.nq.gz
│   ├── 3b61490069b850f823204c209c5875c791af2373.nq.gz
│   ├── 861fbe21564fbea9e0d520f84d0379aed02f1231.nq.gz
│   ├── a800fd6d0d4446ffe620cdaa8acea409d0257614.nq.gz
│   ├── a81c8ee121952cf06bfaf9ff9988edd8cded763c.nq.gz
│   ├── c5799d98512be4339bd4f16b0b0b50e130134ac9.nq.gz
│   ├── d26bbf81885eb3bad079ee90334ff7cc1460c4ee.nq.gz
│   ├── e19f6379ee49bfad8b8dd880f7fafa2e223c2a7f.nq.gz
│   └── ee5869210b583d5231bf3f3c80da752e286fb7b4.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 8f43568693ebd7fcad5c3b79ef6ce0072225914f.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 18 files
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

[waylan/pyyaml-env-tag](https://github.com/waylan/pyyaml-env-tag)

---
*Parsed on 2026-11-06 by [repolex](https://repolex.ai)*
