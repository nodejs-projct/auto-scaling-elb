# auto-scaling-nodejs-app

This github repo hosts the source code for my youtube video where I talked about how to set up auto scaling and load balancing for an node.js express app hosted on AWS EC2 instances (https://www.youtube.com/watch?v=lB3Ip0Yn-Zs).

## Problem
In my case, the error was just `fatal: refusing to merge unrelated histories` on every try, especially the first pull request after remotely adding a Git repository.

### Solution 1.
Using the `--allow-unrelated-histories` flag worked with a pull request in this way:

```bash
git pull origin branchname --allow-unrelated-histories
```
As per `2.9.0 release notes` - git pull has been taught to pass the `--allow-unrelated-histories` option to underlying git merge.

### Solution 2.

Try 
> git pull --rebase development

OR

> git reset --hard origin/master

Eitherway, simply add --allow-unrelated-histories should again, do the trick

> git merge some_branch --allow-unrelated-histories