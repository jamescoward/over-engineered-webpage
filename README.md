# over-engineered-webpage

## Todo

- [x] Run tests on PRs to master
- [x] Deploy to PROD when a PR is merged to master
- [x] Separate PROD and staging AWS accounts and deployments
- [x] Deploy to branch-based staging when PR is opened
- [x] Remove branch-based staging when PR is closed
- [x] Add webpack and babel for bundling and modern JS syntax
- [ ] Add preact for rendering page
- [ ] Run integration tests against branch-based staging env
- [ ] Add building and deploying static assets to s3/something else

Possibly:

- [ ] Create Todo app or something with a database
- [ ] Have separate staging and prod databases
- [ ] Deploy Prod and staging to different AWS accounts
- [ ] Add user authentication with Cognito

## Notes:

Possible way to use stage based table name with fallback

```yml
custom:
  tableNames:
    staging: "dev-table"
    prod: "prod-table"
  calculatedTableName: ${self:custom.tableName.${opt:stage}, self:custom.tableName.staging}
```
