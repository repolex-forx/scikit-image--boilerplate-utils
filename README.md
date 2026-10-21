# Repolex Knowledge Graph of scikit-image/boilerplate-utils

RDF knowledge graph data for [scikit-image/boilerplate-utils](https://github.com/scikit-image/boilerplate-utils), parsed by [repolex](https://repolex.ai).

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
rlex download scikit-image/boilerplate-utils
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 61f29f6feeb5442c6038842a893f991f2d7984af
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 61f29f6feeb5442c6038842a893f991f2d7984af
│           └── chunk-001.nq.gz
├── blob
│   ├── 945b116ad3c50d6d806918539557f3d598810c6f.nq.gz
│   ├── ba4c4b974bf3693675f3d355d27fe9bbd763352c.nq.gz
│   ├── dabec14f5c3e3058f4ebc89dcc746f883f8bef6e.nq.gz
│   └── dbb7dd6cd253bf3a7ef080b94e141ce54c818e17.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 61f29f6feeb5442c6038842a893f991f2d7984af.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 12 files
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

[scikit-image/boilerplate-utils](https://github.com/scikit-image/boilerplate-utils)

---
*Parsed on 2026-10-21 by [repolex](https://repolex.ai)*
