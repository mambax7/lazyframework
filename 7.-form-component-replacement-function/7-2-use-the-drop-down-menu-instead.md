# 7-2 Use the drop-down menu instead

1. edit`admin/main.php`
2. In the background activity management `main.php`, when adding, the "category" must fill in the category number by itself, which is very unfriendly. We can change it to a drop-down menu. ![](https://campus-xoops.tn.edu.tw/uploads/tad_book3/image/47/%E7%81%AB%E7%8B%90%E6%88%AA%E5%9B%BE_2020-05-28T03-44-35.174Z.png)
3. To use the drop-down menu instead, an array of options must be given, the format is:

   ```php
   $option array[option value] = option text;
   ```

4. The option array can be set by yourself, but here, we hope the system can automatically crawl, so we can use it `get_arr($table, $key, $value)`to get the content of a certain table to make a sorted array`：`
   * You must give `$table`\(such as `my_action_cate`:\) to know which table column to grab
   * `$key`Is `cate_id`\(namely the category number\), which is used as the value of the drop-down menu and will be stored in the database.
   * `$value`Is `cate_title`\(namely category title\), used as a drop-down menu option display text.
5. For  `get_arr()` reference: see [API Tutorial](https://xoops.gitbook.io/jill-lazy-framework-api/3.tadmoddata-class/3-1-basic-method/3-1-3-get-the-array-of-the-specified-data-get_arr-usdtable-usdkey-usdvalue)
6. So we can add the following program:

   ```php
   $Model = new TadModData('my_action');
   $clean = $Model->clean();
   // Create category menu
   $cate_arr = $Model->get_arr('my_action_cate', 'cate_id', 'cate_title');
   $Model->use_select('cate_id', $cate_arr);
   ```

7. Then use `use_select($col_name, $options = [])` to be made of an array of menu
   * `$col_name`It refers to which field in the current form should be replaced with a drop-down menu, so we fill in the `cate_id`field.
   * `$options`This is what we just grabbed `$cate_arr`. So far, the application of the drop-down menu has been completed.
8. `use_select()`For details, please refer to: see [API Tutorial](https://xoops.gitbook.io/jill-lazy-framework-api/3.tadmoddata-class/3-4-form-component/3-4-1-drop-down-menu-use_select-usdcol_name-usdoptions)
9. In this way, there will be a menu for direct selection, and the previously filled value will be automatically brought out when editing. ![](https://campus-xoops.tn.edu.tw/uploads/tad_book3/image/47/%E8%A8%BB%E8%A7%A3%202020-05-28%20115106.png)
10. For `use_select()`usage, please refer to: see [API Tutorial](https://xoops.gitbook.io/jill-lazy-framework-api/3.tadmoddata-class/3-4-form-component/3-4-1-drop-down-menu-use_select-usdcol_name-usdoptions)

