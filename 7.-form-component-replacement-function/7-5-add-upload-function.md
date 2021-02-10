# 7-5 Add upload function

1. edit `admin/main.php`
2. When adding an event, if you want to upload some event attachments or photos, you can use this function.
3. This feature requires matching `my_action_files_center` table will have a role.
4. For  `set_file($col_name)`details, please refer to: see [API Tutorial](https://xoops.gitbook.io/jill-lazy-framework-api/3.tadmoddata-class/3-4-form-component/3-4-6-set-as-upload-tool-set_file-usdcol_name)
5. To let the system know who these files belong to, it is necessary to bind a field. We can bind the event number, that is `action_id`, in this way, different events will present different files.

   ```text
   $Model->set_file('action_id');
   ```

6. When editing the event, you can see the upload field. ![](https://campus-xoops.tn.edu.tw/uploads/tad_book3/image/47/%E7%81%AB%E7%8B%90%E6%88%AA%E5%9B%BE_2020-05-28T12-27-37.860Z.png)
7. You can also manage uploaded files while editing ![](https://campus-xoops.tn.edu.tw/uploads/tad_book3/image/47/%E7%81%AB%E7%8B%90%E6%88%AA%E5%9B%BE_2020-05-28T12-35-04.805Z.png)
8. Will automatically appear at the end of the list  ![](https://campus-xoops.tn.edu.tw/uploads/tad_book3/image/47/%E7%81%AB%E7%8B%90%E6%88%AA%E5%9B%BE_2020-05-28T12-42-18.434Z.png)
9. It will also appear below when displaying a single data 

![](../.gitbook/assets/image%20%2813%29.png)

