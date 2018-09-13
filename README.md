# AWS DynamoDB Cross Region Replicator

### Introduction
`ddbr.sh` is a script designed for migrating DynamoDB tables across two regions.  

The tool uses AWS command line tool and mainly AWS Data Pipeline in order to move data across the regions.


### Prerequisites
* `aws` command line tool configured with a profile
* Tables should be already set up in destination region
* S3 bucket(s) required for temporary data storage and logging


### Usage

```text
Usage: ./ddbr.sh [--profile <arg>] [--source-region <arg>] [--destination-region <arg>] [--pipeline-definition <arg>] [--s3-temp <arg>] [--s3-log <arg>] [--table <arg>] [-v|--verbose] [-h|--help]
	--profile: AWS profile (default: 'default')
	--source-region: From region (no default)
	--destination-region: To region (no default)
	--pipeline-definition: Data-pipeline definition (no default)
	--s3-temp: S3 path to store temporary data (no default)
	--s3-log: S3 path to store log files (no default)
	--table: table to replicate (empty by default)
	-v,--verbose: Set verbose output (can be specified multiple times to increase the effect)
	-h,--help: Prints help
```


### Credits
This script was made with help of:
* [Sample DynamoDB cross region copy](https://github.com/aws-samples/data-pipeline-samples/tree/master/samples/dynamodb-to-dynamodb-crossregion)
* [Argbash script skeleton generator](https://argbash.io/)
