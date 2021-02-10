# 9-8 Filter data



1. At present, all registration information is actually listed. If there are other events in the future, they will also be listed here. This is not the result we want. \(Following to add a registration information with a different activity number to the database\) ![](https://campus-xoops.tn.edu.tw/uploads/tad_book3/image/47/%E7%81%AB%E7%8B%90%E6%88%AA%E5%9B%BE_2020-06-01T12-33-48.837Z.png)
2. In theory, just list the applicants for the event, so we can write:

   ```text
   case "show":
       $Model->show($clean['action_id']);
       $ApplyModel->where(['action_id' => $clean['action_id']]);
       $ApplyModel->index();
       break;
   ```

   Then you will get the correct result  
   ![](https://campus-xoops.tn.edu.tw/uploads/tad_book3/image/47/%E7%81%AB%E7%8B%90%E6%88%AA%E5%9B%BE_2020-06-01T12-35-41.007Z.png)

3. For more information, `where()`please refer to: see [API Tutorial](https://xoops.gitbook.io/jill-lazy-framework-api/3.tadmoddata-class/3-3-data-manipulation/3-3-3-filter-data-where-usdwhere_item)
4. At the same time, we can replace the "User ID" with a name, and remove the "Activity ID"

   ```text
   case "show":
       $Model->show($clean['action_id']);
       $ApplyModel->where(['action_id' => $clean['action_id']]);
       $ApplyModel->uid_name();
       $ApplyModel->disable('action_id');
       $ApplyModel->index();
       break;
   ```

   So it looks cleaner  
   ![](https://campus-xoops.tn.edu.tw/uploads/tad_book3/image/47/%E7%81%AB%E7%8B%90%E6%88%AA%E5%9B%BE_2020-06-01T12-39-30.693Z.png)

5. For `uid_name()`reference: see [API Tutorial](https://xoops.gitbook.io/jill-lazy-framework-api/3.tadmoddata-class/3-5-screen-display/3-5-4-change-uid-to-name-to-present-uid_name)
6. For `disable()`reference: see [API Tutorial](https://xoops.gitbook.io/jill-lazy-framework-api/3.tadmoddata-class/3-5-screen-display/3-5-6-fields-not-displayed-disable-usdcol_name)
7. You can also modify the annotations of the database column, and change the "User ID" to "Registrant" ![](https://campus-xoops.tn.edu.tw/uploads/tad_book3/image/47/%E7%81%AB%E7%8B%90%E6%88%AA%E5%9B%BE_2020-06-01T12-41-05.789Z.png)
8. In this way, it is more complete \(remember to revise it too `sql/mysql.sql`~\) 

![](../.gitbook/assets/image%20%2812%29.png)

