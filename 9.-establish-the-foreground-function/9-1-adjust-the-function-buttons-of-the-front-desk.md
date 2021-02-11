# 9-1 Adjust the function buttons of the front desk

1. As long as the administrator logs in \(or the information is published by the current login\), you will see buttons for editing, deleting, adding, etc.
2. But because it is in the foreground, when the button is clicked, editing or adding will be done in the foreground.
3. If we hope to edit and add a button to change the link to the background \(safer, but also more simple\), and even remove the delete button, you can `set_func($func_name, $to)`do:

   ```php
   $Model->set_func('create', 'admin/main.php');
   $Model->set_func('edit', 'admin/main.php');
   $Model->set_func('destroy', false);
   ```

   `set_func()`For a complete description of this, please refer to [API Tutorial](https://xoops.gitbook.io/jill-lazy-framework-api/3.tadmoddata-class/3-4-form-component/3-4-9-reset-function-button-set_func-usdfunc_name)

4. In this way, the screen will be cleaner, and the button will be connected to the background:

![](../.gitbook/assets/image%20%284%29.png)

