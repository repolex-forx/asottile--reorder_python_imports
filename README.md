# Repolex Knowledge Graph of asottile/reorder_python_imports

RDF knowledge graph data for [asottile/reorder_python_imports](https://github.com/asottile/reorder_python_imports), parsed by [repolex](https://repolex.ai).

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
rlex download asottile/reorder_python_imports
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── c64f4b028fa4a84e737010bdec6d6964995c305c
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── c64f4b028fa4a84e737010bdec6d6964995c305c
│           └── chunk-001.nq.gz
├── blob
│   ├── 0102687cd9bfe5a8a5b34a2bf15fb18121e3e44f.nq.gz
│   ├── 0c5a37eb0adeb312718e533d0a4fbcbea6880056.nq.gz
│   ├── 16c4178e5e4a2cab659574318886032b1fc0b9b5.nq.gz
│   ├── 254a07213eb6050f5c507cc1a29b6f550a909c86.nq.gz
│   ├── 3c70e9927de837d97ebb9aebc22b827b22154cea.nq.gz
│   ├── 3d93aefb2da505dba9c0114404cfaaeee5ad0d3f.nq.gz
│   ├── 5370c9485451439199ab7ab9ba30c95d9a046275.nq.gz
│   ├── 671db2f37e9391cfb03957bd7ff963f65d7e84db.nq.gz
│   ├── 6ffab54eebdae6c1a99ca8727f779d60efadde2d.nq.gz
│   ├── 8b041c00a3f91c5d9a2136b4fe6eff1f5ee34dc7.nq.gz
│   ├── 8ceee2d315a5fc21a5aa3389510a90a36ffe2aa2.nq.gz
│   ├── a03e8f656e324eef81514487ad06eb319abf8b79.nq.gz
│   ├── a8c0eb2e6e90b210a3ebe9f45b2ff733d4d46db8.nq.gz
│   ├── cc8138067203f22865a2f3aa3ebd5d4962e0f7e8.nq.gz
│   ├── d145423a5b8aa4c2432fa192d4d4055bbbf73d20.nq.gz
│   ├── d86d9ea06347dbd79c04079484155ea94fa2c3ed.nq.gz
│   ├── dc5942ed876ebca286861fed6ea3199b57aaf60f.nq.gz
│   ├── e5b0edb356ea09e4a7adf251cd7f2b618967eb44.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── ea377fc79826e2f69aa21dac0ef73c13ad8f54dc.nq.gz
│   ├── eaaf2aecf6d149c08d2c9d4c49811cfbda02e599.nq.gz
│   └── ed648d3019e5999b0e81ed9393e687370438c3f5.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── c64f4b028fa4a84e737010bdec6d6964995c305c.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 30 files
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

[asottile/reorder_python_imports](https://github.com/asottile/reorder_python_imports)

---
*Parsed on 2026-10-18 by [repolex](https://repolex.ai)*
