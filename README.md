# Repolex Knowledge Graph of plotly/tutorial-nanodash

RDF knowledge graph data for [plotly/tutorial-nanodash](https://github.com/plotly/tutorial-nanodash), parsed by [repolex](https://repolex.ai).

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
rlex download plotly/tutorial-nanodash
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 4a53766b010a0d6cf643c2dddf825245090014eb
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 4a53766b010a0d6cf643c2dddf825245090014eb
│           └── chunk-001.nq.gz
├── blob
│   ├── 14047057968d5cfa577081ddd9db26e466d34a8c.nq.gz
│   ├── 185618c9f2790c0aff7739e101b607aa879c2276.nq.gz
│   ├── 20c4fbc2a20d5c120c776b8ec8df5a66de5a3e4c.nq.gz
│   ├── 265600dab827b681acedc195c522d93d18de3261.nq.gz
│   ├── 2a9ed9b2ffd0127b95995f815233388813c87904.nq.gz
│   ├── 32179fbc8ad1bd1a9b8246735d6c6475a927bf7e.nq.gz
│   ├── 346a4e5f37b1631235d14e279d841302b6ad8691.nq.gz
│   ├── 35d1f1177acaedb7e2c98cb041f8db21f539ad11.nq.gz
│   ├── 3e44121497980cb11c7a89c5ab97a46258e730dc.nq.gz
│   ├── 513219344aab5d22750ad68c8fe483ce13eb5a8c.nq.gz
│   ├── 5c3da74d7f7d3e24ff0c4c21e4863e9aaf9ae474.nq.gz
│   ├── 5e1f419199468d20710f229b3aa6467e8a1f8394.nq.gz
│   ├── 61830727a04e745a22467c6302db1d02e70f3857.nq.gz
│   ├── 7756b329039829a9fd0cf0f8d7c1a5176224a7fd.nq.gz
│   ├── 7ab5d86f731eced5bb3a8b6127c311bd08d786bb.nq.gz
│   ├── 8320a751a101a6abc4923e4911076061f090ceb2.nq.gz
│   ├── 83a0d778161c6b91192d740799ff5b400dad8903.nq.gz
│   ├── 8ecd359e35034fa6903db2911eabead23f4d49d9.nq.gz
│   ├── 964d989bf483b82c614fee85dc93e5c9367e2e03.nq.gz
│   ├── 97df5ce77a75ca553ed1991a78e2baa1ba8de937.nq.gz
│   ├── 9be06f8a0372a71a1d59fdfc7bfc536a70e1ad25.nq.gz
│   ├── b06ab16978516c3e4bf525e85efebfb992ab2124.nq.gz
│   ├── b5cd767b38939bd5865d9982a8a2eb401083bcfb.nq.gz
│   ├── bb140ed9cca8f51b3a7011c1c5355c527322e830.nq.gz
│   ├── bcaa6072b37b6d2d4665b4f5b4075a0fc97c870a.nq.gz
│   ├── bd8d7a4e85db8e7766dc988f3b0f75a8bfb21220.nq.gz
│   ├── c8de92be0283fe67d0d1bb7923c785237b945dba.nq.gz
│   ├── cfbc7233f3aa07dc28c67ae1c868441b3cf8bfa5.nq.gz
│   ├── d1cc038572ec3a311fe785b220f36d18de0d6418.nq.gz
│   ├── d7eab3f4416b280977abfef0abbde379c05cc212.nq.gz
│   ├── e525a5ff2294565291776a2e8d2a5bf9105ca425.nq.gz
│   ├── e55614afe99fe1c5d9752e9faf0871e40af185be.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── e721efc3a9bbaa733f1bd2f8f178a0005988a951.nq.gz
│   ├── e995b11cd7fc2065ee85c9f74bbb6e059c91b4e1.nq.gz
│   ├── ef2d82034a98a7c6770e8d258b43da90ad6c7bd5.nq.gz
│   ├── f82546e5dd58c7a5637e714fd412762c7951b79a.nq.gz
│   ├── f89e3e27868a3046e35ea7dfb353ea7524338c91.nq.gz
│   └── fa9d18414deb2e778a09ade8f400100b7160ca07.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 4a53766b010a0d6cf643c2dddf825245090014eb.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 46 files
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

[plotly/tutorial-nanodash](https://github.com/plotly/tutorial-nanodash)

---
*Parsed on 2026-11-07 by [repolex](https://repolex.ai)*
