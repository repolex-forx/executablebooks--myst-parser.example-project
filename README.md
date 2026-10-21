# Repolex Knowledge Graph of executablebooks/myst-parser.example-project

RDF knowledge graph data for [executablebooks/myst-parser.example-project](https://github.com/executablebooks/myst-parser.example-project), parsed by [repolex](https://repolex.ai).

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
rlex download executablebooks/myst-parser.example-project
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── da8e9f0a08df098f405c824334eb6dff12ff53a2
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── da8e9f0a08df098f405c824334eb6dff12ff53a2
│           └── chunk-001.nq.gz
├── blob
│   ├── 0086d44d2602cfedbfd20e4405ef83be72076dae.nq.gz
│   ├── 026fdfe315772031f49d4e2eabda7f3834a80838.nq.gz
│   ├── 14b993d8463e755dadf2a4d0e7993cdf0d9da948.nq.gz
│   ├── 17959819f71f09b81b09c9d522d00325e7426e00.nq.gz
│   ├── 1b2e2bd5e55477bc1b165fa1920a3ac8037ae8f3.nq.gz
│   ├── 1f29ca761385ffc466d4c85a28b6d09902643de6.nq.gz
│   ├── 34c65587d352f8ef33b165661d4d92469741667f.nq.gz
│   ├── 3f2657b7c07273db42e722d8cfe0cb6840a91d04.nq.gz
│   ├── 4e340e27e5884bfc76b1bfb3793733c27a3593a0.nq.gz
│   ├── 59168b560317569c423f71fe2d993de263d33013.nq.gz
│   ├── 6511501712b55a1834000c1f6cd3f8f5218db692.nq.gz
│   ├── 682d5d144b8ce7b4e079e5c224ba8c34c27b7728.nq.gz
│   ├── 72de03cde2321244999625b9b0201f81846487de.nq.gz
│   ├── 8561661fb5a7b63a7caf9ef8b6fc9080bbf105b0.nq.gz
│   ├── 88a353048b43a1d8b51765454874f6ba62854fca.nq.gz
│   ├── 8bae54d95b0304251e3821cc837d5f8db284905c.nq.gz
│   ├── 8bd9af3f5a5ac29272d278f539171a27ac7e7096.nq.gz
│   ├── 9383852e831d12bed38d6aab15f40f726d727ee5.nq.gz
│   ├── a108cb8b86a5701f614cca6866e825b09f802395.nq.gz
│   ├── b541d57dfa94d793758f938dc20ae5672cba2e90.nq.gz
│   ├── b8c0a5d97ba342a0d7f521b7cb8d3f46c3a3d9c1.nq.gz
│   ├── cc6d2a19e40c79c873e71c4c382457df6672cb01.nq.gz
│   ├── dad2d2a6d2a6501493fe497a848e8053350b23a7.nq.gz
│   ├── ead45c8a13802fdec31506a9db43732e952f9278.nq.gz
│   └── f5f27098c5b8e7fd822aa8056d12fb0c54f76d21.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── da8e9f0a08df098f405c824334eb6dff12ff53a2.nq.gz
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

[executablebooks/myst-parser.example-project](https://github.com/executablebooks/myst-parser.example-project)

---
*Parsed on 2026-10-21 by [repolex](https://repolex.ai)*
