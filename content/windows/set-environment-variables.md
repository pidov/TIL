+++
title = "Setting environment variables (command line)"
weight = 5
date = "2016-11-06T00:40:33+02:00"
+++

### Set environment variables in the current prompt.

```ps
set NODE_ENV=development
```

{{% notice note %}}
set.exe does not set the environment variable in subsequent command prompts. The variables are only available in the currently opened prompt.
{{% /notice %}}

### Set persistent environment variables

```ps
setx NODE_ENV=development
```

{{% notice note %}}
setx.exe does not set the environment variable in the current command prompt, but it will be available in subsequent command prompts.
{{% /notice %}}

### List all environment variables

```ps
set
```
Output:
```ps
ALLUSERSPROFILE=C:\ProgramData
APPDATA=C:\Users\user\AppData\Roaming
.
.
```
