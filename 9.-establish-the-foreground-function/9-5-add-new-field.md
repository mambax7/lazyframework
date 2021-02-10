# 9-5 add new field

1. At present, there is only one button left in the registration interface, which is a little lonely. If you want to add a new field such as: contact number, what should I do?
2. Very simple, go to the database management interface and modify the data table: ![](https://campus-xoops.tn.edu.tw/uploads/tad_book3/image/47/%E7%81%AB%E7%8B%90%E6%88%AA%E5%9B%BE_2020-06-01T06-33-41.735Z.png)
3. Just add a field directly ![](https://campus-xoops.tn.edu.tw/uploads/tad_book3/image/47/%E7%81%AB%E7%8B%90%E6%88%AA%E5%9B%BE_2020-06-01T06-36-01.604Z.png)
4. In this way, refresh the screen and you can use it! ![](https://campus-xoops.tn.edu.tw/uploads/tad_book3/image/47/%E7%81%AB%E7%8B%90%E6%88%AA%E5%9B%BE_2020-06-01T06-36-59.857Z.png)
5. Remember to re-export the database structure and update to`sql/mysql.sql`

   ```php
   ...略...
   CREATE TABLE `my_action_apply` (
     `apply_id` smallint(5) unsigned NOT NULL AUTO_INCREMENT COMMENT '報名編號',
     `uid` smallint(6) NOT NULL COMMENT '使用者編號',
     `action_id` smallint(6) NOT NULL COMMENT '活動編號',
     `phone` varchar(255) NOT NULL COMMENT '聯絡電話',
     `apply_date` datetime NOT NULL COMMENT '報名時間',
     PRIMARY KEY (`apply_id`)
   ) ENGINE=MyISAM DEFAULT CHARSET=utf8;
   ...略...
   ```

6. Finally, we add a required field and verify by phone, it will be more complete. For verification, [please see API Tutorial](https://xoops.gitbook.io/jill-lazy-framework-api/3.tadmoddata-class/3-4-form-component/3-4-8-set-as-required-field-set_require-usdcol_name) :

   ```php
   $ApplyModel->set_require('phone', ['custom' => 'phone']);
   ```

   ![](https://campus-xoops.tn.edu.tw/uploads/tad_book3/image/47/%E7%81%AB%E7%8B%90%E6%88%AA%E5%9B%BE_2020-06-01T11-59-24.922Z.png)

