# 8-4 Add link



1. edit`main.php`
2. At present, you can only use the URL to watch a single event, which is very troublesome. Therefore , it is much more convenient `action_title`to add a link directly to the "event title" `main.php?op=show&action_id=Activity ID`.
3. We can use `set_link($col_name)`grammar to put the link, it can be multiple groups.
4. `set_link()`For details, please refer to [API Tutorial](https://xoops.gitbook.io/jill-lazy-framework-api/3.tadmoddata-class/3-5-screen-display/3-5-7-add-link-set_link-usdcol_name) 
5. E.g:

   ```php
   $Model->set_link('action_title', 'main.php', ['op' => 'show', 'action_id']);
   ```

6. In this way, the activity title field in the list part will add the link we specified: 

![](../.gitbook/assets/image%20%281%29.png)

