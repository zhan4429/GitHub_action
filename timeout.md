## Timeout
Kill the job if the jobs run more than certain time. 
```
deploy:
    timeout-minutes: 10 # The job will be terminated after running 10 mins.
    steps:
    - name: Docker Run
      timeout-minutes: 1 # The step will be terminated after running 1 min.
```