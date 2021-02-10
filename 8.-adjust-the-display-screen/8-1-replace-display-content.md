# 8-1 Replace display content



1. edit`admin/main.php`
2. At present, our classification still displays a number \(whether in a list or a single data\), so it is not easy to understand, it should directly display the name of the classification: In addition, the "Enable or Not" part also displays a number. ![](https://campus-xoops.tn.edu.tw/uploads/tad_book3/image/47/%E7%81%AB%E7%8B%90%E6%88%AA%E5%9B%BE_2020-05-28T13-12-43.230Z.png)  ![](https://campus-xoops.tn.edu.tw/uploads/tad_book3/image/47/%E7%81%AB%E7%8B%90%E6%88%AA%E5%9B%BE_2020-05-28T13-15-27.215Z.png)
3. We can use it `replace('Replaced field', $replacementValueArray)`to replace the displayed data.

   ```text
   $cate_arr = $Model->get_arr('my_action_cate', 'cate_id', 'cate_title');
   $enable_arr = [1 => 'Enabled', 0 => 'Disabled'];
   ...略...
   $Model->replace('cate_id', $cate_arr);
   $Model->replace('enable', $enable_arr);
   ```

   1. `$cate_arr`It was originally captured. The array index is the category number `$cate_id`, and the array value is the category title. We just used it `cate_id`, which means replacing the `$cate_id`number with the Chinese category title.
   2. `$enable_arr`It is an array made by yourself. The `$enable`value used for replacement will be `1`replaced with "enabled" and it will be `0`replaced with "off".

4. In this way, no matter in the list or single data, it has been replaced with the result we want  

![](../.gitbook/assets/image%20%2810%29.png)

![](../.gitbook/assets/image%20%283%29.png)

