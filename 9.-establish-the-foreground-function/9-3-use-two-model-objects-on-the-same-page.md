# 9-3 Use two model objects on the same page

1. The front page of the front desk is basically used for registration, and the registration is another data sheet, but because the front page needs to display the registration data and also allows users to register, we need to create another model object `$ApplyModel`responsible for registration and a `my_action_apply`data table Various related operations.

   ```php
   $ApplyModel = new TadModData('my_action_apply');
   ```

2. In addition, in terms of routing, all new registrations, amendments, and deletions are `$ApplyModel`related. Therefore, the method used must be `$ApplyModel`the same method. As for the incoming parameter filtering, the original `$clean`can be used \(because the incoming variable is not filtered Data sheet used\):

   ```php
   ...略...

   switch ($op) {
       case "create":
           $ApplyModel->create();
           break;

       case "edit":
           $ApplyModel->edit($clean['apply_id']);
           break;

       case "show":
           $Model->show($clean['action_id']);
           break;

       case "update":
           $ApplyModel->update($clean['apply_id']);
           header("location:{$self}");
           exit;

       case "store":
           $ApplyModel->store();
           header("location:{$self}");
           exit;

       case "destroy":
           $ApplyModel->destroy($clean['apply_id']);
           header("location:{$self}");
           exit;

       default:
           $Model->index();
           break;
   }
   ```

3. Only `index`and `show`is the model object of the activity `$Model`\(because it is used to display the activity, not to register\)

