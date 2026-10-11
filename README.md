# Repolex Knowledge Graph of aio-libs/aioloop-proxy

RDF knowledge graph data for [aio-libs/aioloop-proxy](https://github.com/aio-libs/aioloop-proxy), parsed by [repolex](https://repolex.ai).

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
rlex download aio-libs/aioloop-proxy
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── ab9a19d098c1e5454aaabb9222a6787e71af541e
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── ab9a19d098c1e5454aaabb9222a6787e71af541e
│           └── chunk-001.nq.gz
├── blob
│   ├── 06df68ef6926dad12de01085305f66873dcf9dbb.nq.gz
│   ├── 18366ca3a2d73b788f498df2287df54edccb697a.nq.gz
│   ├── 261eeb9e9f8b2b4b0d119366dda99c6fd7d35c64.nq.gz
│   ├── 286afde12f0babe363ef377c7d1c9f177665cf43.nq.gz
│   ├── 355f4e91636ff68c65e88db19759f465c2a730a2.nq.gz
│   ├── 4f7a4befdb78594b3d0769a4f1f3806981bfc8e4.nq.gz
│   ├── 56d6e5075e9a4dcd46693e834e1b7a8f5beacb94.nq.gz
│   ├── 593cccabe028b2b0d1cf8742b1296367acc8b28e.nq.gz
│   ├── 5ed598031ea827fd00cd1396870dee43e5dfb8ca.nq.gz
│   ├── 606849326a4002007fd42060b51e69a19c18675c.nq.gz
│   ├── 648e6912ca91765c13b4414dd76f056d96d00da9.nq.gz
│   ├── 68f1dde695b01d09e02478909db2309fbe7933be.nq.gz
│   ├── 6e7b53a779551188cfefb7b221ccf9cf0dd67da6.nq.gz
│   ├── 756e3cc6b90647b92ff52ccab31ab3896815641f.nq.gz
│   ├── 7d5fd1fbd6fd47640269bf5c21ee0bdf63aae740.nq.gz
│   ├── 864badf6f0ab4beed8e6ddb443e0a24987fe9a22.nq.gz
│   ├── 8701bd928e9c420205a31969c0f3403d2333a3ea.nq.gz
│   ├── 8c7ee9b0162412b33b517d28bbc9fbd92ca0fdae.nq.gz
│   ├── 8e8dff1bfadf3684a70166fb8aae443420c1aed7.nq.gz
│   ├── 91e302d6e6788811617cd16c84673859d4dd1bfd.nq.gz
│   ├── 97af74efaae686a7fc730b9d4d686a174d50293f.nq.gz
│   ├── 99c2f2e7cad3e125740447b0e270e4f3d57fe467.nq.gz
│   ├── 9ce06a81ea45b2883a6faf07a0d2136bb2a4e647.nq.gz
│   ├── a19543394f3adfc769d7464220526a91cbdae4f0.nq.gz
│   ├── a211cdf937a13f19f9a749957456867a1aea7f0a.nq.gz
│   ├── a5348a5fa8c52450471502e8fe5c18cce98df3cd.nq.gz
│   ├── a68229d8887dedf3b8be7846398857d245c7565b.nq.gz
│   ├── adc163629793a4a9aa1e9076df7fe18a60f61d5e.nq.gz
│   ├── c7d6462a25fa9bf416df6d2fa60541659c28bfe8.nq.gz
│   ├── c8f202ad78a55ec076e35d80237de8bf79a41b6a.nq.gz
│   ├── cbfa987493dd2654f249b1d6d1b3f7c156157b01.nq.gz
│   ├── d1a8e269a561790ec756a4f7dcae74f3c2d9f4c1.nq.gz
│   ├── df90a2ffed2aabbc501ef9f2084d928cdd8d46c2.nq.gz
│   ├── ee2dd7a2a345f7ca3c8fc02fc0c0fa44f9d77081.nq.gz
│   ├── fbea9a0d7bc847050f706c758974e58b20dba11e.nq.gz
│   ├── ff2f2f229d9fe0df99f050eea44f1bcc7d11fe6e.nq.gz
│   └── fff312721b22e53ef5717803b361f19a0fd53e80.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── ab9a19d098c1e5454aaabb9222a6787e71af541e.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 44 files
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

[aio-libs/aioloop-proxy](https://github.com/aio-libs/aioloop-proxy)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
