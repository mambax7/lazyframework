# 7-3 Replace the option value of a single selection

1. edit`admin/main.php`
2. In the background activity management `main.php`, when adding, the "Enable or Not" option is displayed `1`and `0`we can replace it with Chinese. ![](https://campus-xoops.tn.edu.tw/uploads/tad_book3/image/47/%E7%81%AB%E7%8B%90%E6%88%AA%E5%9B%BE_2020-05-28T06-42-18.063Z.png)
3. The principle is the same as the drop-down menu of the previous unit, except that the method is changed `use_radio($col_name, $options = [])` . The applied field is "Enable or Not", and the field name is `enable`. For the option array part, we use a homemade option array: `[1 => '啟用', 0 => '關閉']`no need to go to which table to grab produce.

   ```text
   $Model->use_radio('enable', [1 => '啟用', 0 => '關閉']);
   ```

4. In this way, the options will be replaced by our customized options, and the previously filled values ​​will be automatically brought out when editing. ![](https://campus-xoops.tn.edu.tw/uploads/tad_book3/image/47/%E7%81%AB%E7%8B%90%E6%88%AA%E5%9B%BE_2020-05-28T06-48-13.699Z.png)
5. For `use_radio()`complete usage, please refer to: [https://campus-xoops.tn.edu.tw/modules/tad\_book3/page.php?tbsn=48&tbdsn=1618](https://campus-xoops.tn.edu.tw/modules/tad_book3/page.php?tbsn=48&tbdsn=1618)

