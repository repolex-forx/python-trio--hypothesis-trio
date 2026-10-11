# Repolex Knowledge Graph of python-trio/hypothesis-trio

RDF knowledge graph data for [python-trio/hypothesis-trio](https://github.com/python-trio/hypothesis-trio), parsed by [repolex](https://repolex.ai).

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
rlex download python-trio/hypothesis-trio
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 84250f4e35491e55959eff1d48a420b18aa98e60
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 84250f4e35491e55959eff1d48a420b18aa98e60
│           └── chunk-001.nq.gz
├── blob
│   ├── 1366ea4c46b9b5310b80e1f9baf64f0a2ca403ee.nq.gz
│   ├── 1e73cf1b1a67c558b2c826d5730ee849a555eda8.nq.gz
│   ├── 291bfeaa3b207e4173c50080f22cfb473363ee5a.nq.gz
│   ├── 373e614a3cd7ec4a1985d0b6ca8000d001714f52.nq.gz
│   ├── 45893b8ebaa713d5ec3d5f04ed05c8046e4ad945.nq.gz
│   ├── 4edd4b18b3f9a2893c3d0a37e5e747a5f09cebe7.nq.gz
│   ├── 54871c8ea6a98ca4e7410fe28fff03018584170b.nq.gz
│   ├── 5c1d0224860d4402e9c930603dfb2f7065e6e657.nq.gz
│   ├── 5fa2f81c34e093b7b461f6c88dc3ec49dcdd3970.nq.gz
│   ├── 6a8ec4c68c194bc888a44e6ff47e408e131e9f77.nq.gz
│   ├── 87456116e9f4df1fce3c6530bb4e8c578f32715e.nq.gz
│   ├── 8dfcf08bfae66df02b66a4034c791e0b57fefc0f.nq.gz
│   ├── 8f0d2678baa9502c3c672f82a9b2c49679f1a293.nq.gz
│   ├── 91c1e69c703e498f5b813aab01e4b87f327a65e6.nq.gz
│   ├── 9e27fc0cdf01b4f4c4f1fca3055ab0ae02e411cd.nq.gz
│   ├── a5c4dc0daac1fc6261796495ab09ef7075a65702.nq.gz
│   ├── a6770c6d4f84803535046704576df44f92f3950a.nq.gz
│   ├── acb7cebc375502a3dee2c68e76c0a34b096a3d8e.nq.gz
│   ├── ae10048ba947c2958a7413860317e8038bf4689b.nq.gz
│   ├── b38f1a56edac686f29b4e1c99c1fa8fe0f488f04.nq.gz
│   ├── c80415d63f62acb8e4b48f05dc1416b1e1ce903e.nq.gz
│   ├── d9913f56dfdec8c03b551f8f919b57b853d18028.nq.gz
│   ├── da318666f7849f9365210cd7cf7630474b5997da.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── e9bb1c6118f499cf404ae670eb9a5b14a92f1e61.nq.gz
│   ├── fa0086a952236971ab37901954d596efae9f4af6.nq.gz
│   └── fbf510ea93223a1d6e959ff9159e43c31afdfada.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 84250f4e35491e55959eff1d48a420b18aa98e60.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 35 files
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

[python-trio/hypothesis-trio](https://github.com/python-trio/hypothesis-trio)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
