# Repolex Knowledge Graph of langchain-ai/fleet-deepagents-export

RDF knowledge graph data for [langchain-ai/fleet-deepagents-export](https://github.com/langchain-ai/fleet-deepagents-export), parsed by [repolex](https://repolex.ai).

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
rlex download langchain-ai/fleet-deepagents-export
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 9fb264ca6a942e83b459a5c0ed6057735ed6736a
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 9fb264ca6a942e83b459a5c0ed6057735ed6736a
│           └── chunk-001.nq.gz
├── blob
│   ├── 0507650d975dee1df7722d5aef0b37d06481448a.nq.gz
│   ├── 0aa224d9fe843a6897928a4f2d0079aeb9ce9eaa.nq.gz
│   ├── 0f986c7362a62f66544c33295e9d5a32203dd92a.nq.gz
│   ├── 227d2f8d0a7ad4c7022bed332ec41299dfe108be.nq.gz
│   ├── 32e73cc9577c8a7a5f8a2f46410c815d4ace9603.nq.gz
│   ├── 3602487d6137a0fd9a02c67d3aa51bd0445b4eff.nq.gz
│   ├── 3957738673765912ca83a0048f833e095d61e087.nq.gz
│   ├── 65f8cd3c25089aa331db12fef1f6828f96c5a9b6.nq.gz
│   ├── 6c7c2e94b460f8160258c2ff1d982a20f3e7281f.nq.gz
│   ├── 73208368e2b099a83e94db25fe6536cd150415a8.nq.gz
│   ├── 7aabfd6c2d0e7db27277bc1ccf1e46a65011922a.nq.gz
│   ├── 7fc63232d7a320ec35b8073a7691af4dc0bc150e.nq.gz
│   ├── 8b18f4998b7d810c9670d9364a6b2df1697ce76c.nq.gz
│   ├── 8b4f5b28e09a83a38667a6aea69ff9c5b4e112c8.nq.gz
│   ├── 8f9557415c68a5f1c7a37a656a6e4b2b38d4f5dc.nq.gz
│   ├── 9e687aa2c182d1e74c866c6dba01fd50696056ab.nq.gz
│   ├── a01376567a4a7a86c5495b609489ddcae2193bb1.nq.gz
│   ├── c593f1576861cd571287c9ac37ff1917c24c6575.nq.gz
│   ├── c896b0829aef54ab93328943232f498e99978be8.nq.gz
│   ├── d45176beabe30781c04cdfc9849660183ed71588.nq.gz
│   ├── e39ce4aae070a19998772117966670e13d42611a.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── e6cf5921b6b4296cf0a0052a1d70d47125ad3e9c.nq.gz
│   ├── ecaa1dcc3de2e0a85548b06d32956c4cce2b8c45.nq.gz
│   └── eee205d4a03e57835e90265765bf1b36e17824c5.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 9fb264ca6a942e83b459a5c0ed6057735ed6736a.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 33 files
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

[langchain-ai/fleet-deepagents-export](https://github.com/langchain-ai/fleet-deepagents-export)

---
*Parsed on 2026-11-08 by [repolex](https://repolex.ai)*
