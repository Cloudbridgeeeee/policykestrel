# Proposed AWS architecture

| Service | Role |
|---|---|
| S3 | Encrypted storage for policy PDFs, kept per brokerage |
| Textract | Text and tables read from scanned policy pages |
| Bedrock | Clauses matched and plain-language summaries drafted |
| Lambda and DynamoDB | Comparisons, review status and the sign-off log |

One AWS account per customer, encrypted at rest and in transit. The public demo calls none of these services.
