# Repolex Knowledge Graph of gruntjs/grunt-contrib-copy

RDF knowledge graph data for [gruntjs/grunt-contrib-copy](https://github.com/gruntjs/grunt-contrib-copy), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [lexq](https://github.com/repolex-ai/lexq) query tool using [uv](https://docs.astral.sh/uv/getting-started/installation/).

If you have uv installed, just copy/paste this into your terminal:

```bash
uv tool install git+https://github.com/repolex-ai/lexq
```

This installs lexq onto your system, in your user context. Verify the install:

```bash
lexq --help
```

**lexq is designed to be used primarily by LLMs in a terminal.** Start up your favorite LLM and ask it to use the lexq tool. It's that easy!

To load this repo's data:

```bash
lexq download gruntjs/grunt-contrib-copy
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 85150c7bfef1279911cb844eefdcd7b2c31ad9d1
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 85150c7bfef1279911cb844eefdcd7b2c31ad9d1.nq.gz
│   └── repolex
│       └── 85150c7bfef1279911cb844eefdcd7b2c31ad9d1
│           └── chunk-001.nq.gz
├── blob
│   ├── 1961cf057845ada81899de440b20255d0766d38a.nq.gz
│   ├── 2125666142eb661091cc5f32af2ed2f3fc65571d.nq.gz
│   ├── 241f7e990a4726a94e4fc2412bb12d88c223fde5.nq.gz
│   ├── 507f91281ddb349f4b46006c67c28165b7690cf6.nq.gz
│   ├── 578bc95edfdd03851a468675170c038f090bb3b5.nq.gz
│   ├── 57ec08e12f642db602643427b4c444a9aeb4251a.nq.gz
│   ├── 5961d019b8733f04af80cccd3a2ce83adb965d21.nq.gz
│   ├── 5cb6bfd4d74d1d9cca0e57c40ce8855378b78d86.nq.gz
│   ├── 5d08cc3879a0bcb62e516656f4b929150e4ec64c.nq.gz
│   ├── 67ecb0ee926b8cfc73bf777d8b51d87155ff80a4.nq.gz
│   ├── 68bec77a10810fa5e9f6e558b04bf0aa50249986.nq.gz
│   ├── 707b19e693bd54c2e909ba8fe667acde94af291f.nq.gz
│   ├── 9227a3f50cd0e7a6173d6e4b155cff02cee26b8e.nq.gz
│   ├── 92ffcda567f9d363979624d13b00ca74bfaae491.nq.gz
│   ├── 98751ccf604e03cb3ac450dab57edf16a1eba71c.nq.gz
│   ├── a112b5938178414a91cd117377bd6f4666b37084.nq.gz
│   ├── ac7972ffad3efcddc561d8febaba9e551554062d.nq.gz
│   ├── b2bba779da8586bbb7714b2ff8c4cce31655b7f7.nq.gz
│   ├── bdb476cdc50d0cf5a0bdf40cbe22f6d43ec3972c.nq.gz
│   ├── c0d0bdc8b95cb01a9203ea3618694685e28b7aab.nq.gz
│   ├── c6d58d5cc24c0cdc254a5e2a01aa6515715f9fd9.nq.gz
│   ├── de4091ed38f60328ea5cba06514e9193a96c3c3b.nq.gz
│   ├── ea17b22ee52e2dbd806e0f69f8c19fad29bdbf6d.nq.gz
│   └── f0c452b9989a88112687f8e6abd5a1ae13b3dbd8.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 85150c7bfef1279911cb844eefdcd7b2c31ad9d1.nq.gz
├── filetree
│   └── 85150c7bfef1279911cb844eefdcd7b2c31ad9d1.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 34 files
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

## Source repository

[gruntjs/grunt-contrib-copy](https://github.com/gruntjs/grunt-contrib-copy)

---
*Parsed on 2026-04-13 by [repolex](https://repolex.ai)*
