# ELB logs to ELK

Brings up ELK stack using `docker-compose`, fetches ELB logs from S3 and stores them in Elasticsearch.

Kibana is available on port `5601`.

```bash
S3_BUCKET=X \ 
   S3_PREFIX=Y \
   AWS_REGION=Z \ 
   AWS_ACCESS_KEY_ID=A \ 
   AWS_SECRET_ACCESS_KEY=Z \
   docker-compose up
```

## Environment variables

| ENV | description | example |
| --- | --- | --- |
| S3_BUCKET | S3 bucket where ELB logs are stored |
| S3_PREFIX | path inside S3 bucket where ELB logs are stored | `AWSLogs/XXXXXXXXXXXX/elasticloadbalancing/us-east-1/2018/04/20` |
| AWS_REGION | S3 bucket / ELB region | `us-east-1` |
| AWS_ACCESS_KEY_ID | AWS access key |
| AWS_SECRET_ACCESS_KEY | AWS secret key |

