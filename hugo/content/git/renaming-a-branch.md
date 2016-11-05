+++
title = "Renaming a branch"
weight = 5
date = "2016-11-06T00:20:55+02:00"

+++

#### Renaming a branch locally and remotely:

1. Switch to branch which needs to be renamed

```
git branch -m <new_name>
git push origin :<old_name>
git push origin <newname>:refs/heads/<new_name>
```
