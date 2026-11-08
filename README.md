# Repolex Knowledge Graph of UKPLab/eacl2026-abcd-link

RDF knowledge graph data for [UKPLab/eacl2026-abcd-link](https://github.com/UKPLab/eacl2026-abcd-link), parsed by [repolex](https://repolex.ai).

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
rlex download UKPLab/eacl2026-abcd-link
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 93296424f5940f797818583a4a475f96669f3deb
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 93296424f5940f797818583a4a475f96669f3deb
│           └── chunk-001.nq.gz
├── blob
│   ├── 0107f6b4e4a64344c4f6f017de4b7798882ee5c8.nq.gz
│   ├── 011ee1b08d2cf43057fb64bd0c8ec894ea3eb0fa.nq.gz
│   ├── 04db9e390b73241a2ec0cf8d396ffcd9ad52ff5f.nq.gz
│   ├── 06cf2b408f7e619eb1ee211b5703cd73a6d2ec69.nq.gz
│   ├── 0ba3aec492a710368aded0a725c95c5baa2585e5.nq.gz
│   ├── 0d9360dc35d158ea1ccd025d9520994762579eec.nq.gz
│   ├── 120c6893b8af8f69dddc51b2734ed561b78c6091.nq.gz
│   ├── 1883f8b61b76efef491927be4b3b9957cbca8371.nq.gz
│   ├── 33b333c9d9430b26770242d50a94e911a54f410a.nq.gz
│   ├── 35dc4e615541470b683ea4472a8a48cb0511ad27.nq.gz
│   ├── 3ac6612f69f5e31d7785c4d04d576c1b6d65c458.nq.gz
│   ├── 3f4415cf757a879e6cc17692b705a194e2a135f3.nq.gz
│   ├── 4494992e95a890d760734ccf84e8f96ba53b132e.nq.gz
│   ├── 4cef27e61ea9ac6f982e68a89dcb12432298bb71.nq.gz
│   ├── 6b94e4503a06eba4ff7b03aad85ecb60923a665a.nq.gz
│   ├── 72b16e7f37debfbbb0d507e737ad55676a0fe071.nq.gz
│   ├── 77e71743aff60239563bd80d8841d89e2d3f2575.nq.gz
│   ├── 83eeb26c767b126bdae56d3346cf69475598d244.nq.gz
│   ├── 8a32ee34b1603953ed79a91dec01453f67fb93c4.nq.gz
│   ├── 90cab153ae7f7d0b61b20fd0c643449151a8ca3c.nq.gz
│   ├── 9ccc7363dcc9155dec920e64a9820737d3fff0e3.nq.gz
│   ├── b513db01bd79b64de1f11f946d883c2d982a810d.nq.gz
│   ├── b66b76bdff90a5d4e80ee7f5e66993effc06a867.nq.gz
│   ├── b9320f2f8920e77d6c9f34a4c5d663c7be65d051.nq.gz
│   ├── cc98b6933cd0df2705fd39225f24282258cd3685.nq.gz
│   ├── da1dc36b73b09ed01f70d46e38a806ba5e1a6a68.nq.gz
│   ├── ea6d05ea8f9d193059c6b06318dbcc5229e7b33a.nq.gz
│   ├── f50b79f2f8d0399dcbe24fcf668696f0d78a9d02.nq.gz
│   ├── f537286d8d4df9648cdbdaf5298281c3edee2c48.nq.gz
│   ├── f59e00d41e3fd23e40f752f7f1b3117184e2eedd.nq.gz
│   ├── fc195968226a7e8515654b28d783294e0ed770e8.nq.gz
│   └── ffe00e966fc94d736de409dbd208e770acf395c9.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 93296424f5940f797818583a4a475f96669f3deb.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 39 files
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

[UKPLab/eacl2026-abcd-link](https://github.com/UKPLab/eacl2026-abcd-link)

---
*Parsed on 2026-11-08 by [repolex](https://repolex.ai)*
