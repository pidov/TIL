# Renaming a branch

Renaming a branch locally and remotely:

1. Switch to branch which needs to be renamed

```
git branch -m <new_name>
git push origin :<old_name>
git push origin <newname>:refs/heads/<new_name>
```

