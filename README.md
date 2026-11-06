# Repolex Knowledge Graph of sphinx-contrib/sphinxcontrib-del-marker

RDF knowledge graph data for [sphinx-contrib/sphinxcontrib-del-marker](https://github.com/sphinx-contrib/sphinxcontrib-del-marker), parsed by [repolex](https://repolex.ai).

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
rlex download sphinx-contrib/sphinxcontrib-del-marker
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── e9a327e2b93b3f2d0ba8318a2f938868a1a434e3
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── e9a327e2b93b3f2d0ba8318a2f938868a1a434e3
│           └── chunk-001.nq.gz
├── blob
│   ├── 027aec8fa4c4c92c013c30749bc6e8d456e3b275.nq.gz
│   ├── 22e75b797b1f356754cde9f579414d2c93befcdc.nq.gz
│   ├── 26b22668b0a16fd733ffc9d7420b442196164985.nq.gz
│   ├── 26ed3ca04929caf9d44b657a183ddc83aba1628d.nq.gz
│   ├── 4ec62ac87035090da4bcf04874384858c2cbe407.nq.gz
│   ├── 6c56a2d2c84805f0415396a1d7bfb7c204e8356a.nq.gz
│   ├── 88f08461b9ae55344a4607f357db9d8f2faddce5.nq.gz
│   ├── d0c3cbf1020d5c292abdedf27627c6abe25e2293.nq.gz
│   ├── d902344aae5b78e56607ee2b394b9df51723c7b8.nq.gz
│   ├── dc1312ab09ca6fb0267dee6b28a38e69c253631a.nq.gz
│   ├── dc76ab6aea31f31c5044617d455c20f461097816.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   └── fa93de23d2adb904e10e5263a5eff6d32c02d072.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── e9a327e2b93b3f2d0ba8318a2f938868a1a434e3.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 20 files
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

[sphinx-contrib/sphinxcontrib-del-marker](https://github.com/sphinx-contrib/sphinxcontrib-del-marker)

---
*Parsed on 2026-11-06 by [repolex](https://repolex.ai)*
