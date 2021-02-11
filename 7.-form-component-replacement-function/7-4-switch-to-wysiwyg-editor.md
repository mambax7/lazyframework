# 7-4 Switch to WYSIWYG editor

1. edit`admin/main.php`
2. When adding an event, the "event description" is currently a simple large text box, we can change it to CKEditor WYSIWYG editor
3. For `use_ckeditor($col_name)` details, please refer to: see [API Tutorial](https://xoops.gitbook.io/jill-lazy-framework-api/3.tadmoddata-class/3-4-form-component/3-4-3-wysiwyg-editor-use_ckeditor-usdcol_name)
4. The applied field is "Activity Description", and its field name is `action_content`; to set the array part, use to `setHeight`set the height of the editing area, and use the `setToolbarSet`setting toolbar \(the number of functions varies\)

   ```php
   $Model->use_ckeditor('action_content', ['setHeight' => 150, 'setToolbarSet' => 'tadSimple']);
   ```

5. In this way, the "Activity Description" will be replaced by a WYSIWYG editor.

![](../.gitbook/assets/image%20%286%29.png)

