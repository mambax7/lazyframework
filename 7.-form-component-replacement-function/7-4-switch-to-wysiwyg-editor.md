# 7-4 Switch to WYSIWYG editor

1. edit`admin/main.php`
2. When adding an event, the "event description" is currently a simple large text box, we can change it to CKEditor WYSIWYG editor
3. For `use_ckeditor($col_name)` details, please refer to: [https://campus-xoops.tn.edu.tw/modules/tad\_book3/page.php?tbsn=48&tbdsn=1619](https://campus-xoops.tn.edu.tw/modules/tad_book3/page.php?tbsn=48&tbdsn=1619)
4. The applied field is "Activity Description", and its field name is `action_content`; to set the array part, use to `setHeight`set the height of the editing area, and use the `setToolbarSet`setting toolbar \(the number of functions varies\)

   ```text
   $Model->use_ckeditor('action_content', ['setHeight' => 150, 'setToolbarSet' => 'tadSimple']);
   ```

5. In this way, the "Activity Description" will be replaced by a WYSIWYG editor. ![](https://campus-xoops.tn.edu.tw/uploads/tad_book3/image/47/%E7%81%AB%E7%8B%90%E6%88%AA%E5%9B%BE_2020-05-28T07-47-55.896Z.png)

