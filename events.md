## workflow_dispatch
```
on: workflow_dispatch
```
Allow you to run this workflow manually from the actions tab. 

## pull request

```
pull_request:
    type: [opened]
```

The action requires the approval from maintainers. If the PR is from the contributor, the action will always be activated.

## Schedule
```
schedule:
    - cron: '*/5 * * * *' ## Runs every 5 mins
```