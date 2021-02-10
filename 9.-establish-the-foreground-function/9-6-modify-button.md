# 9-6 Modify button

1. "Adding information" looks weird and it is not easy for ordinary users to understand, so it is more straightforward to change to "I want to register".

   ```text
   $ApplyModel->set_submit('op', 'store', '我要報名', 'fa-plus');
   ```

   ![](https://campus-xoops.tn.edu.tw/uploads/tad_book3/image/47/%E7%81%AB%E7%8B%90%E6%88%AA%E5%9B%BE_2020-06-01T12-01-43.681Z.png)

2. For `set_submit()`the usage, please refer to: [https://campus-xoops.tn.edu.tw/modules/tad\_book3/page.php?tbsn=48&tbdsn=1621](https://campus-xoops.tn.edu.tw/modules/tad_book3/page.php?tbsn=48&tbdsn=1621)
3. After clicking "I want to sign up", from the database, I did see that a record was added ![](https://campus-xoops.tn.edu.tw/uploads/tad_book3/image/47/%E7%81%AB%E7%8B%90%E6%88%AA%E5%9B%BE_2020-06-01T12-02-37.276Z.png)

