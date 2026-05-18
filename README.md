# ITC 6050 - Week 1 Lab
## What dlt did automatically
1. **Schema inference** — detected column names and data types from the GitHub API JSON response automatically
2. **Table creation** — created the `github_issues` table in PostgreSQL without writing any SQL
3. **Pagination handling** — managed multiple API pages automatically without manual loops

## How dlt handled nested JSON
- Nested objects (like `user`) were flattened into columns using 
  double underscore notation (e.g. `user__login`, `user__id`)
- dlt inferred all data types automatically (bigint, boolean, 
  timestamp, varchar) from the API response
- Arrays like `labels` were handled by creating separate child tables