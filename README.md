SimpleTriggeredJob
==================

This demonstrates create, deploy and run a simple triggered job.

1. Create an Azure WebSites.
2. Clone and push this repository to your site.  This will deploy the `simplejob` to the appropriate location.
3. List the existing jobs by browsing to `<scm_url>/jobs`.  You should see one job named `simplejob` with `run_command` pointed to `run.cmd`.
4. Run the job by `curl -X POST <scm_url>/jobs/triggered/simplejob/run -d ''`.   This will start the `run.cmd`.
5. See the job status by browsing to `<scm_url>/jobs/triggered/simplejob`.  The latest_run status represents the last run status.
6. To diagnose issue, see the job stdout/stderr by browsing to `output_url` and `error_url` respectively.   Notice `Hello World` echo-ed from `run.cmd` when viewing the `output_url`.

That's it.
