# Repolex Knowledge Graph of asimov-modules/asimov-brightdata-module

RDF knowledge graph data for [asimov-modules/asimov-brightdata-module](https://github.com/asimov-modules/asimov-brightdata-module), parsed by [repolex](https://repolex.ai).

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
rlex download asimov-modules/asimov-brightdata-module
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 8d75b5594590bf09aabd8d092bbc26603a2f924b
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 8d75b5594590bf09aabd8d092bbc26603a2f924b.nq.gz
│   └── repolex
│       └── 8d75b5594590bf09aabd8d092bbc26603a2f924b
│           └── chunk-001.nq.gz
├── blob
│   ├── 2391f73aa051d3804285ce744f2e9a1c7e08993d.nq.gz
│   ├── 2b26fe1557e6a4d3b1e8d716e404d3c22d3f51ae.nq.gz
│   ├── 4f7e10d54f47fd014b87e7519814c23eedfbc114.nq.gz
│   ├── 4ff4a460349224ae04b31da8e7d2629a03de90ee.nq.gz
│   ├── 5431a85a6c8741f7f45fffb195bd41e121e834c9.nq.gz
│   ├── 5a0b0b4975cd8251c7ee1296c2c9268ad089a8f0.nq.gz
│   ├── 5a5831ab6bf692d5c93e7784852b0b5a05c153b4.nq.gz
│   ├── 5f5107c56fac686357e5e8bd87ef2bfe816fa9b0.nq.gz
│   ├── 5f5cf896c81688e4360b37f1bcda92f7bc6f7423.nq.gz
│   ├── 6a45c5270c7d9f703198704f91d6b227eedeee0e.nq.gz
│   ├── 6b23d61018f43b840f8d2ff3b45a1c02d76df38d.nq.gz
│   ├── 6ba866027bb83f440142c6a4d8563035a9071e88.nq.gz
│   ├── 734ceb90bbbe0a02b0278eee6e13bbed7e06653c.nq.gz
│   ├── 75e3b65f99b29f48ab230e3eab3de8d0b7a9229f.nq.gz
│   ├── 761e2859180af426c06adea2131f0830267e8665.nq.gz
│   ├── 7b3063f6cb8b4a718737b0cbd52e48f77d10455e.nq.gz
│   ├── 870cd847ca182f0255b84ce590e3295497319e3e.nq.gz
│   ├── 88544301dca052e504d8dbb999796db7db250fd3.nq.gz
│   ├── 92d2cd551170df7931e8a0d43dbc6cf831c92965.nq.gz
│   ├── 92eebb56c57e27daa4f87c2684c59f1efe848448.nq.gz
│   ├── 97d97f278241634449dc0960af06e2fef00200bd.nq.gz
│   ├── 99a4cf5bee130fd824434491a355594e516ca5f2.nq.gz
│   ├── 9c558e357c41674e39880abb6c3209e539de42e2.nq.gz
│   ├── a36fedab8db68b26a76fbbf1de1f549e4a12261b.nq.gz
│   ├── af9908b08f4b33c32a0080af73f53bc0fa0cdce4.nq.gz
│   ├── afb9caada5f740f3ce8ca88a903cdff67d86b8f0.nq.gz
│   ├── b8f4bf8643c842f9c66cc12f4f6e458225f33ac3.nq.gz
│   ├── c49728c3d71aa5343a7115bc1602de51b778c518.nq.gz
│   ├── c96f3aa6a1c21d46ce9fe1a39d8475e5ae1b2791.nq.gz
│   ├── cf42f6893594e2f8be2b722de51123d65e4d61c4.nq.gz
│   ├── d1c30d9d5caefdad6749220eb41228c0a9e8b8fa.nq.gz
│   ├── e09589b1a9b29c0d11e3be48c9cce66fb1ccb48e.nq.gz
│   ├── e3e57a8ce4ccbf74759a6df8fa4a3980ff1c9209.nq.gz
│   ├── efb98088164f5786b17e83ed384971fc3c74f93c.nq.gz
│   ├── f22a095fb8a2ec0291674479eac463c035e1c1a7.nq.gz
│   └── f45ac1df1a8ced7306b2ab042ff62d12bfe88c61.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 8d75b5594590bf09aabd8d092bbc26603a2f924b.nq.gz
├── filetree
│   └── 8d75b5594590bf09aabd8d092bbc26603a2f924b.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

14 directories, 45 files
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

[asimov-modules/asimov-brightdata-module](https://github.com/asimov-modules/asimov-brightdata-module)

---
*Parsed on 2026-09-28 by [repolex](https://repolex.ai)*
