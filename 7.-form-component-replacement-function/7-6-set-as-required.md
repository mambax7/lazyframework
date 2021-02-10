# 7-6 Set as required



1. edit`admin/main.php`
2. If you want "Activity Title", "Activity Date", and "Registration Deadline" to be required, and the "Activity Title" has at least three characters and a maximum of 30 characters, then please set it like this:

   ```php
   $Model->set_require('action_title', ['minSize' => 3, 'maxSize' => 30]);
   $Model->set_require('action_date');
   $Model->set_require('action_end_date');
   ```

   ![](https://campus-xoops.tn.edu.tw/uploads/tad_book3/image/47/%E7%81%AB%E7%8B%90%E6%88%AA%E5%9B%BE_2020-06-01T08-29-41.266Z.png)  

3. `set_require()`For usage, please refer to: [https://campus-xoops.tn.edu.tw/modules/tad\_book3/page.php?tbsn=48&tbdsn=1624](https://campus-xoops.tn.edu.tw/modules/tad_book3/page.php?tbsn=48&tbdsn=1624)

