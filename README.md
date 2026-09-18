# uptime-watchdog

Checks the Apex Hub API health endpoint every 10 minutes. If it fails three attempts in a row, this opens an "API is down" issue in the private `Kipnetic/apex-hub` repo, and closes it once health returns.

The repo is public because Actions minutes are free on public repositories. The only secret is `APEX_ISSUES_TOKEN`, a fine-grained token that can only read and write issues in `Kipnetic/apex-hub`.

A weekly keepalive commit stops GitHub switching off the schedule after 60 days without activity.
