# 7-1 Add automatic sorting and pull sorting functions



1. edit`admin/cate.php`
2. Just at the time of publication classification, sorting themselves to fill in, and does not automatically take the maximum, in addition, it can not be easy to sort of pull, then you can use `set_sort($col_name)`to add this feature, please refer to the detailed description: [API Tutorial](https://xoops.gitbook.io/jill-lazy-framework-api/3.tadmoddata-class/3-4-form-component/3-4-7-set-as-sort-field-set_sort-usdcol_name)
3. `my_action_cate`In, the field responsible for sorting records is `cate_sort`, so fill it in.

   ```text
   $Model = new TadModData('my_action_cate');
   $Model->set_sort('cate_sort');
   ```

4. In this way, when adding, it will automatically find the maximum value of the sort.![](https://campus-xoops.tn.edu.tw/uploads/tad_book3/image/47/%E7%81%AB%E7%8B%90%E6%88%AA%E5%9B%BE_2020-05-28T02-53-33.845Z.png)
5. In the list, you can also directly pull to adjust the order. ![](https://campus-xoops.tn.edu.tw/uploads/tad_book3/image/47/%E8%A8%BB%E8%A7%A3%202020-05-28%20161343.png)
6. So far, the classification management function in the background has been quite complete.

