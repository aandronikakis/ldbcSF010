## Instructions

 0. Combine ldbc.jar parts to a single ldbc.jar file
```
 cat ldbc.jar.parta* > ldbc.jar
```

 1. Start Neo4j Server
```
 ./neo4j-enterprise-x.x.x/bin/neo4j console
```

 2. Configure LDBC Load Generator (see `ldbc_snb_interactive_SF-0010-read-cypher.properties`):
 * `neo4j.url` (e.g., `bolt://localhost:7687`)
 * (OPTIONAL) `thread_count` (default: `4`)
 * (OPTIONAL) `warmup` (default: `10000` operations)
 * (OPTIONAL) `operation_count` 
 * (OPTIONAL) `results_dir` (default: `benchmark_results/`)

 3. Generate Load
```
java -jar ldbc.jar run --ldbc-config ldbc_snb_interactive_SF-0010-read-cypher.properties
```
