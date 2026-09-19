# mine_search_text

L0 retrieval and L1 ML filter on top of OpenSearch.

## Responsibilities
- Turn criteria into one OpenSearch query: candidate sources (`knn`, `covis`, `popular`) + filters.
- L1 ML filter: `script_score` linear model over doc values and request features, `min_score` + per-shard top-K.
- Return the merged top-N with source flags. Owns the ML filter model.

## Technologies
- HTTP API
- OpenSearch (BM25, filtered kNN, hybrid, `script_score`)
