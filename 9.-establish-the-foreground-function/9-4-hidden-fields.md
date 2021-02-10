# 9-4 Hidden Fields



1. If you click "I want to register", then `create`this action will be executed , that is, a registration profile will be created. It should be noted that this `create`is a `$ApplyMode`model object, so that the information can be written in the `my_action_apply`registration data form.

   ```text
   ...略...
   $ApplyModel = new TadModData('my_action_apply');

   switch ($op) {
       case "create":
           $ApplyModel->create();
           break;
   ...略...
   ```

2. Remember to modify the template `template/op_index_create.tpl`\(and the edited template `template/op_index_edit.tpl`\), the screen will appear correctly:

   ```text
   <{$toolbar}>

   <{$my_action_apply_form}>
   ```

3. The screen currently looks like this: ![](https://campus-xoops.tn.edu.tw/uploads/tad_book3/image/47/%E7%81%AB%E7%8B%90%E6%88%AA%E5%9B%BE_2020-06-01T03-24-16.975Z.png)
4. It’s too funny to let applicants fill in the number by themselves. Besides, our link also brings the number to this page. Therefore, in fact, we can change the "Activity Number" field to a hidden form and change `action_id`the value Brought in automatically.
5. In addition, the "registration time" is not recommended for users to fill in by themselves. It is inhumane, and it is troublesome to fill in incorrectly. Therefore, it can also be hidden.
6. We use it `set_hidden($col_name, $def_val)`to achieve this. For detailed usage, please refer to: [https://campus-xoops.tn.edu.tw/modules/tad\_book3/page.php?tbsn=48&tbdsn=1620](https://campus-xoops.tn.edu.tw/modules/tad_book3/page.php?tbsn=48&tbdsn=1620)

   ```text
   ...略...
   $ApplyModel = new TadModData('my_action_apply');
   $ApplyModel->set_hidden('action_id', $clean['action_id']);
   $ApplyModel->set_hidden('apply_date', date("Y-m-d H:i:s"));

   switch ($op) {
       case "create":
           $ApplyModel->create();
           break;
   ...略...
   ```

   1. `$col_name`: Refers to the field to be replaced, so fill in`action_id`
   2. `$def_val`: It is the value of the field, so fill it in `$clean['action_id']`, that is , the value of the activity number passed in. For date and time, we can use it `date()`to grab the current time.

7. In this way, "Activity Number" and "Registration Time" become hidden fields: ![](https://campus-xoops.tn.edu.tw/uploads/tad_book3/image/47/%E8%A8%BB%E8%A7%A3%202020-06-01%20142301.png)

