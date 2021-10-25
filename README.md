# Migration Instructions

When updating the congress member data we need to get a new data csv. Use the current or past csv as a template.

`congress.csv` will always be the current data to import.

Archive the old csv by changing it's name to congress[MM][YY].csv

See the status of the congress_member migration
```
drush migrate-status congress_member
```

Remove all existing imported data
```
drush migrate-rollback congress_member
```

Import the new data from `congress.csv`
```
drush migrate-import congress_member
```
