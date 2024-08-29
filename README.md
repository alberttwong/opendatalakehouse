# Data Lakehouse Readiness Score

The Data Lakehouse Readiness Score is a quantitative measure that assesses a database's vendor support of Apache Iceberg, Apache Hudi and Delta Lake. 

|                        | Data Lakehouse Readiness Score |
| ---------------------- | ------------------------------ |
| Clickhouse             | R                              |
| StarRocks \| CelerData | R\*W\*                         |
| Apache Druid \| Imply  | R                              |
| PrestoDB               | R\*W\*                         |
| TrinoDB \| StarBurst   | R\*W\*                         |
| DuckDB \| Motherduck   | R                              |
| AWS Redshift           | R                              |
| GCP BigQuery           | R                              |
| Snowflake              | R\*W\*                         |
| Polars                 | R\*W\*                         |
| Daft                   | R\*W\*                         |
| AWS Athena             | R\*W\*                         |
| AWS Redshift Spectrum  | R\*W\*                         |
| Dremio                 | R\*W\*                         |
| Databend               | R                              |
| SingleStore            | R\*W\*                         |
| Umbra DB \| CedarDB    | No Data                        |

Key:
* R = Can read at least one of the open table formats
* R*W* = Can read and write at least one of the open table formats
* RW = Can read and write all 3 of major open table formats
