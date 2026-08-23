# Couchbase Magma

<p class="note-meta">August 2026</p>

Magma is Couchbase's storage engine for large, write-heavy datasets. It is designed to keep storage efficient when the working set is much larger than available memory.

> Choose the engine around the workload, not around a default.

## Couchstore vs. Magma

Couchstore is a strong fit when the active working set can largely stay in memory. Magma is intended for larger datasets where disk access and write amplification become primary concerns.

| Criterion | Couchstore | Magma |
| --- | --- | --- |
| Minimum bucket memory quota | 100 MB | 1 GB |
| Minimum memory-to-data ratio | 10% | 1% |
| Maximum data per node | ~3 TB | ~10 TB |
| Best fit | Working set fits mostly in memory | Working set substantially exceeds memory |
| Storage access | Memory-cache oriented | Disk-access oriented |
| Hardware | Can run on lower-end hardware | Benefits from higher-quality hardware |
| Typical use | Memory-led access patterns | Large, durable, write-heavy data |

## Why Magma matters

Magma aims to:

- increase storage density and write throughput per node;
- reduce write amplification; and
- extend SSD lifetime under sustained write load.

For a deeper background, see Couchbase's [Magma storage engine overview](https://www.couchbase.com/blog/magma-next-gen-document-storage-engine/).

## Rule of thumb

Use Magma when capacity and sustained writes matter more than keeping the entire active dataset in memory. Validate the choice with your own data shape, access pattern, latency budget, and recovery requirements.
