# 9-7 Use two model objects on a single page

1. Several people have signed up, but how can the administrator see who has signed up? The easiest way is to list the registered information below when watching a single event.
2. Therefore, we can in `switch`the `show`inside, using the `my_action_apply`model object to the registration list now list:

   ```php
   case "show":
       $Model->show($clean['action_id']);
       $ApplyModel->index();
       break;
   ```

3. At the same time, remember to change the template. The current file is the `index.php`execution action `show`. Therefore, the template file is `op_index_show.tpl`, open the modification

   ```php
   <{$toolbar}>
   <h2 class="my"><{$my_action.action_title}></h2>
   <{$my_action_show}>

   <h2 class="my">已報名名單</h2>
   <{$my_action_apply_index}>
   ```

4. Because you are using `$ApplyModel->index();`, in other words, `my_action_apply`a `index`list, the framework will automatically generate a `<{$my_action_apply_index}>`template label for application, and the label will list all the registration lists.

![](../.gitbook/assets/image%20%288%29.png)

