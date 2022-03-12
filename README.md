# My own notes for diplomas thesis

When I want to fetch new things from the original repostitory I can use the next
article:
https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/syncing-a-fork

But before I need to verify if I have set up the upstream (original ReaR):
```
$ git remote add upstream https://github.com/ORIGINAL_OWNER/ORIGINAL_REPOSITORY.git
```
more here: https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/configuring-a-remote-for-a-fork


## Make check
### Via Packit

I added the make validate into rear.spec file:
https://github.com/antonvoznia/rear/commit/ddc8551bd9e32488c9cede7361f198cdfb8b0a4a
Now before the build it validates the ReaR's code.

The example of pull request with the validating on:
https://github.com/antonvoznia/rear/pull/38
