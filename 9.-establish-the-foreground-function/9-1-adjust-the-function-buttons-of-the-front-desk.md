# 9-1 Adjust the function buttons of the front desk



1. As long as the administrator logs in \(or the information is published by the current login\), you will see buttons for editing, deleting, adding, etc.
2. But because it is in the foreground, when the button is clicked, editing or adding will be done in the foreground.
3. If we hope to edit and add a button to change the link to the background \(safer, but also more simple\), and even remove the delete button, you can `set_func($func_name, $to)`do:

   ```text
   $Model->set_func('create', 'admin/main.php');
   $Model->set_func('edit', 'admin/main.php');
   $Model->set_func('destroy', false);
   ```

   `set_func()`For a complete description of this, please refer to: [https://campus-xoops.tn.edu.tw/modules/tad\_book3/page.php?tbsn=48&tbdsn=1625](https://campus-xoops.tn.edu.tw/modules/tad_book3/page.php?tbsn=48&tbdsn=1625)

4. In this way, the screen will be cleaner, and the button will be connected to the background: ![](https://campus-xoops.tn.edu.tw/uploads/tad_book3/image/47/%E7%81%AB%E7%8B%90%E6%88%AA%E5%9B%BE_2020-05-29T08-11-43.273Z.png)

