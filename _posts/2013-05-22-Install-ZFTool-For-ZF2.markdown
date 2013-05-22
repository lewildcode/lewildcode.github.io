---
layout: post
title: Installing ZFTool for Zend Framework 2
author: timoziemann
category: zf2
tags: zf2
year: 2013
month: 5
day: 22
published: false
summary: While playing around with the ZFTool module for the Zend Framework 2, I noticed some issues with the CLI setup.
image: post_two.png
---

So I checked out the README file at
the [ZFTool module](https://github.com/zendframework/ZFTool/blob/master/README.md)
the other day. I've added the repo to my composer.json file and tried to call
the zf.php from the command line. But it seems it didn't find my actual modules.

Currently, there are some steps missing in the README file, how you have to go
on after installing the ZFTool module via composer (or similar). To set everything
up, you'll have to:

### First: modify your composer.json file to look like this
'''js
{
    "require": {
        "php": ">=5.3.3",
        "zendframework/zendframework"   : "2.*",
        "zendframework/zftool"          : "dev-master"
    }
}
'''

### Second: add it to your application.config.php "modules" section:
'''php
return array(
    'modules' => array(
        'Application',
        'ZFTool',
        // ...
    )
);
'''

Now you may use your command line like `php public/index.php --version` or any
other command available via ZFTool.

There is one more thing: if you are using the `module_map_cache_enabled` and
`config_cache_enabled` settings (set them to active) you possibly have a cached
classmap. So you'll possibly have to clear the cache folder :-)

Stay tuned,
Timo