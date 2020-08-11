# vital-fedora3-plus
Support for vital fedora3 plugin for fedora versions 3.5+

Example redbox configuration:
In your system-config.json or config-include folders, under `transformerDefaults`

```"vital": {
....
    "datastreams": {
....
    },

"redirects": {
 "dsID": "REDIRECT%02d",
 "status": "A",
 "label": "Download",
 "controlGroup": "R",
 "versionable": false,
 "retainIds": true,
 "locationFields": [
    "dc:relation.bibo:Website"
 ]
},
"attachments": {
}
}
```

So notice that 'redirects' is on the same level as 'datastreams' and 'attachments' in the config.

The locationFields is a list of either tfpackage numbered base keys or just a simple string key name.

