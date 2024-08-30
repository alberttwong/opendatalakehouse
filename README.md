# Data Lakehouse Readiness Score

The Data Lakehouse Readiness Score is a quantitative measure that assesses a database's vendor support of Apache Iceberg, Apache Hudi and Delta Lake using a data catalog like Hive Metastore (HMS), Glue, Snowflake Catalog, or Unity Catalog.  
|                        | Table Format | Catalog           | Score |
| ---------------------- | ------------ | ----------------- | ----- |
| Clickhouse             | R\*          | \-                | 0     |
| StarRocks \| CelerData | R\*W\*       | HMS, Glue         | 3     |
| Apache Druid \| Imply  | R\*          | \-                | 0     |
| PrestoDB               | R\*W\*       | HMS, Glue         | 3     |
| TrinoDB \| StarBurst   | R\*W\*       | HMS, Glue         | 3     |
| DuckDB \| Motherduck   | R\*          | \-                | 0     |
| AWS Redshift           | R            | Glue              | 1     |
| GCP BigQuery           | R\*          | \-                | 0     |
| Snowflake              | R\*W\*       | Snowflake         | 3     |
| Polars                 | R\*W\*       | HMS, Glue         | 3     |
| Daft                   | R\*W\*       | HMS, Glue         | 3     |
| Apache Spark           | RW           | HMS, Glue         | 5     |
| AWS Athena             | R\*W\*       | Glue              | 3     |
| AWS Redshift Spectrum  | R\*W\*       | Glue              | 3     |
| Dremio                 | R\*W\*       | HMS, Glue         | 3     |
| Databend               | R            | HMS               | 1     |
| SingleStore            | R\*          | Glue, Snowflake   | 0     |
| Umbra DB \| CedarDB    | No Data      | \-                | 0     |

Scoring:
* RW = 5 points, R\*W\* = 3 points, R = 1 point
  
Key:
* R\* = Can read at least one of the open table formats
* R = Can read at least one of the open table formats using a data catalog
* R\*W\* = Can read and write at least one of the open table formats using a data catalog
* RW = Can read and write all 3 of major open table formats using a data datalog

### Additional Reading
* [Apache Hudi vs Delta Lake vs Apache Iceberg - Data Lakehouse Feature Comparison](https://www.onehouse.ai/blog/apache-hudi-vs-delta-lake-vs-apache-iceberg-lakehouse-feature-comparison)
* [2024 Lakehouse Format Rundown: Engines & Gorillas](https://blog.sundeck.io/2024-lakehouse-format-rundown-7edd75015428)
  * Some good stuff in there but biases?.  Read the comments to the article.  Also he doesn't accept PRs (eg. see my PR that has been waiting for months) and some of the data is out of date. 
* [Why some OLAP databases are faster than others](https://github.com/alberttwong/databasecomparison)
* [Why are there benchmarks for some databases but not for others? You can thank Oracle and where are we now?](https://atwong.medium.com/why-are-there-benchmarks-for-some-databases-but-not-for-others-80f628f0b679)
* [Open Source and Closed Source OLAP databases that can run TPC-H and TPC-DS benchmarks](https://atwong.medium.com/olap-databases-that-can-run-tpc-h-and-tpc-ds-benchmarks-6b4e5300f45b)
