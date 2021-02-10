---
description: >-
  Added preference settings for xoops_version.php (not necessary, multiple
  groups can be used)
---

# 2-2 Preference settings

Each set of settings will generate a set of preferences in the background preferences \(keep annotated if you don't need them, or you can set them again later\):

```php
$TadMod->add_config('show_num', 'Number of data displayed per page', '', 'textbox', 'int', 20);
```

When the module is installed, a set of preferences will be generated such as:

![](https://campus-xoops.tn.edu.tw/uploads/tad_book3/image/47/%E7%81%AB%E7%8B%90%E6%88%AA%E5%9B%BE_2020-05-29T03-32-26.456Z.png)

Full method description: [see here](https://xoops.gitbook.io/jill-lazy-framework-api/2.tadmod-class/untitled/2-2-add-preferences-add_config-usdname)

