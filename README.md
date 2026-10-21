# Repolex Knowledge Graph of joblib/threadpoolctl

RDF knowledge graph data for [joblib/threadpoolctl](https://github.com/joblib/threadpoolctl), parsed by [repolex](https://repolex.ai).

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
rlex download joblib/threadpoolctl
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── ca1677b5259b1e20f01dc8f5378717889b1e893a
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── ca1677b5259b1e20f01dc8f5378717889b1e893a
│           └── chunk-001.nq.gz
├── blob
│   ├── 01190bdbf9dddfa9d0a13af35d472e7e2485e704.nq.gz
│   ├── 02343d19a4fd96a6424514969a1ed4378946fe02.nq.gz
│   ├── 0e643c662dca38c45858c169fed88bfd25b0a948.nq.gz
│   ├── 118556528e97a14b3fcf136593c426fd587610a0.nq.gz
│   ├── 1d7302bf83b056e8bb3f53437ada712f2e94e9c2.nq.gz
│   ├── 2295de63412757a7a330cfc89e15fee4bc1c695d.nq.gz
│   ├── 2426d48da9e65fef3892a276ff1506e720673b92.nq.gz
│   ├── 29ea90f452f78ec67570a15b732fc17e03f0eb16.nq.gz
│   ├── 2b7d606561d5ae829a61be97ebac0ad309329202.nq.gz
│   ├── 2eab17c3663d6c4f398b8ee316db327f69d8762a.nq.gz
│   ├── 31175756d3da92bcc027feb448bdb6aa27b177ea.nq.gz
│   ├── 31800fcfbeadc1e502be456d818393f2e8bf7482.nq.gz
│   ├── 387f3b4cb6964d2845106e13ba39bb5698b2628a.nq.gz
│   ├── 4bc27696382ae684668cbd0c406b1f4a2dfa4f32.nq.gz
│   ├── 566e7f4cb435f6f1fb0df508993fc9760e184cae.nq.gz
│   ├── 5d7707f514ef2a6e3ff097bee51caa51eac550d1.nq.gz
│   ├── 623b0324396084047d9575ee7d3126390fe09d07.nq.gz
│   ├── 6b1277111f42b07566be15228db27cc17641f4d1.nq.gz
│   ├── 6fb013bdbc188ccce116b5d30e1d88031640a891.nq.gz
│   ├── 73a6c1f64541d5c9836ee1ab5798cbf9b5fcb680.nq.gz
│   ├── 8ac5550c4d8d1105f0bab03f788b3a5ed8dd45d3.nq.gz
│   ├── 8da2cb917aae4926f5fd528ee0ee261448c9e19e.nq.gz
│   ├── 90356b33e9333cf6379d8f2978e4f733d8267ee0.nq.gz
│   ├── 9bfcfe23ec26312722bdc8c2162b007318c6be0b.nq.gz
│   ├── 9cdfb2c15ab5b2c48ede1a30edda68bdd96ac23b.nq.gz
│   ├── a5c9b8fab595d71d73a0a8b30007075ce93764a8.nq.gz
│   ├── a77143566795d96c510dc8cf5e4cffb4bf2df9da.nq.gz
│   ├── ad3ef185520838c0f12d9d35a049b751ddd119ed.nq.gz
│   ├── b38ed7d77d3e8a826579a299e46dc2d30e88ab36.nq.gz
│   ├── b9ec8d8eb8095278a491742ed89257c69f89af02.nq.gz
│   ├── c47e7dba5fc6fbd9036be9f0cd2516aa3946b924.nq.gz
│   ├── d38dfe70640f78e424d114ee221664b308ad918b.nq.gz
│   ├── d76291e7391e067b135d146ab1ae0bc703ffc6fc.nq.gz
│   ├── d98aa93af4d0fb43054de188a49fb70c9939b943.nq.gz
│   ├── db2472009c60acc72ca2f6f065bb4b674dc66746.nq.gz
│   ├── e3120d6e25cc68552c441c7cdb2db426fe1dccab.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── edf505c0d56f7938f1bbe66d29cffa0d310884d0.nq.gz
│   └── f4d0852cc6653bd74353e968d8cfebaf2255bb25.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── ca1677b5259b1e20f01dc8f5378717889b1e893a.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 47 files
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

[joblib/threadpoolctl](https://github.com/joblib/threadpoolctl)

---
*Parsed on 2026-10-21 by [repolex](https://repolex.ai)*
