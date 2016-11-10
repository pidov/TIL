+++
date = "2016-11-10T12:00:14+02:00"
title = "Beautify json string in the console"
weight = 5

+++
Sometimes, while debugging (e.g. REST APIs with cURL) it's useful to be able to display correctly formatted and indented json. The following command helps with that:

```
python -mjson.tool json-file-to-beautify.json
```

Example usage with curl
```
curl https://ipidov.com/api/users | python -mjson.tool 
```

