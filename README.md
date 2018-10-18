# go vet with expanded message format

Default format: `filename:line: issue-text`

New format: `filename:line:issue-name:issue-usage issue-text`. Example: 
```bash
vendor\\db1.go:123:printf:check printf-like invocations: missing argument for Fatalf(\"%#x\"): format reads arg 5, have only 4 args
```

This could be used for CI/Analysis tools where issue name/usage is needed for grouping and/or UI purposes.
