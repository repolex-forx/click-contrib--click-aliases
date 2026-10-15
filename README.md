# Repolex Knowledge Graph of click-contrib/click-aliases

RDF knowledge graph data for [click-contrib/click-aliases](https://github.com/click-contrib/click-aliases), parsed by [repolex](https://repolex.ai).

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
rlex download click-contrib/click-aliases
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 8341453c076dc616cd6e02aeaae13e2be73a46af
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 8341453c076dc616cd6e02aeaae13e2be73a46af
│           └── chunk-001.nq.gz
├── blob
│   ├── 19a18deab7412af2a14ebaa5ce80180f7202cfb0.nq.gz
│   ├── 2f8a9c6d9a96093c5dcd38d984dde52e4de846fa.nq.gz
│   ├── 3c6e79cf31da1c0433d2fa666bf50b53f6359f26.nq.gz
│   ├── 50ac6becb7ded698d99b8fc33f423738a4dcf23a.nq.gz
│   ├── 59e1908d0b0d5bc316a00557868517477f087f48.nq.gz
│   ├── 637f60c814ff5ddefa903fbcfff445efa8aae1d2.nq.gz
│   ├── 7b48b8b66b007100502dcacfe4ce1133af5d9872.nq.gz
│   ├── 998397e9f7b1ac6c031bdbf76a45a982c8c829ae.nq.gz
│   ├── acbb23312481e75f636d30724c1b7b71ae30bff0.nq.gz
│   ├── b7a704be54722c86962dc1e5128550cf854800e1.nq.gz
│   ├── b9c707300d7fbe971530fbb357c071602657e85f.nq.gz
│   ├── bcfb18e190490159f9847afe1109faf379f8a536.nq.gz
│   ├── ccbcdb2db31efe2586da78f6494c85fa494b4748.nq.gz
│   ├── d18ed1d6870396412c9a8e6354f267673440bf13.nq.gz
│   ├── d4f4510f6b645e0f7e1dad9a25ce588633cb450f.nq.gz
│   ├── d58872e1c888ee58141dfdcc06b932ddc27a9ce9.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── f2a43b211d192cacb122830eecafb2e06c5e0ff0.nq.gz
│   ├── f497ee1a3fd7fcb1626331219982c88a1de77675.nq.gz
│   ├── f7aa7f40252265252e65221991e190c8a806a7b2.nq.gz
│   └── ff26e78dc5a3e43079d1c33f2fb638b0f46dba02.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 8341453c076dc616cd6e02aeaae13e2be73a46af.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 29 files
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

[click-contrib/click-aliases](https://github.com/click-contrib/click-aliases)

---
*Parsed on 2026-10-15 by [repolex](https://repolex.ai)*
