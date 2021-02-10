---
description: >-
  2-3 Added block settings for xoops_version.php (not necessary, multiple groups
  can be used)
---

# 2-3 Block settings

Each setting of a group will generate an applicable block in the background block \(Of course, you must also generate the block program and template file by yourself in the future. The same, keep the comment status if you don’t need it, or you need it later Set it again\):

```text
$TadMod->add_blocks('action_list', '活動一覽', '', ['顯示資料數' => 5]);
```

When the module is installed, an installable block will be generated \(but it doesn’t matter whether it works, it depends on whether you have completed the block content\)

![](https://campus-xoops.tn.edu.tw/uploads/tad_book3/image/47/%E7%81%AB%E7%8B%90%E6%88%AA%E5%9B%BE_2020-05-29T03-34-08.335Z.png)

Full method description: [https://campus-xoops.tn.edu.tw/modules/tad\_book3/page.php?tbsn=48&tbdsn=1640](https://campus-xoops.tn.edu.tw/modules/tad_book3/page.php?tbsn=48&tbdsn=1640)

