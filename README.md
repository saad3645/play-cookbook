# Description

Chef cookbook for installing [Play framework](http://www.playframework.com/).


This cookbook is experimental and a work in progress until otherwise mentioned. Please test vigorously if you use this in a production environment. Otherwise Bon Appétit. :)


## Platform

- Amazon Linux
- Ubuntu 12.04*


## Cookbooks

This cookbook depends on the following cookbooks:
- [java](http://community.opscode.com/cookbooks/java)


## Attributes

### Play installation

|Key              |Type    |Description                 |Default|
|-----------------|--------|----------------------------|-------|
|`version`        |`String`|The Play version to install.|`2.2.2`|
|`base_url`       |`String`|The base url for downloading Play.|`http://downloads.typesafe.com/play`|
|`download_url`   |`String`|The fully formed url for downloading Play. This is contructed by concatenating the `version` with the `base_url`. **Note** that if this attribute is overriden then the `base_url` becomes defunct and is ignored.|`{base_url}/{version}/play-{version}.zip`|
|`download_prefix`|`String`|The download path           |`/tmp` |
|`install_prefix` |`String`|The installation path       |`/opt` | 
|`home`           |`String`|The name of Play's home directory|`play-2.2.2`| 


<br/>
**Example usage**

```json
{
  "play": {
    "version": "2.2.2",
    "base_url": "http://downloads.typesafe.com/play",
    "download_url": "http://downloads.typesafe.com/play/2.2.2/play-2.2.2.zip",
    "download_prefix": "/tmp",
    "install_prefix": "/opt",
    "home": "play-2.2.2"
  }
}
```

## Contributing

If your are a ruby guy, please contribute. This cookbook was made by a developer who knows nothing of ruby. You can surely improve the code.


## License and Authors

This cookbook is based on and greatly influenced by several other play2 cookbooks written by various authors and contributors before this. Much of the credit for this cookbook goes to these developers. My special thanks to:

Andrea Minetti for https://github.com/minettiandrea/play2


<br/>
_The java cookbook is included just for completeness._

<br/>
**LICENSE**: Unless otherwise stated, the cookbooks/recipes in this repository are licensed under the Apache 2.0 license. See the LICENSE file for full description. Some files are just imported and authored by others. Their license will of course apply.
