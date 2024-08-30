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
* Some of the raw data to create the score can be found at https://github.com/sundeck-io/tableformats.
  * However he doesn't accept PRs (eg. see my PR that has been waiting for months) and some of the data is out of date. 
* [Why some OLAP databases are faster than others](https://github.com/alberttwong/databasecomparison)
