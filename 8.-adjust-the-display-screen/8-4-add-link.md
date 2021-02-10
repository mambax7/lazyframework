# 8-4 Add link



1. edit`main.php`
2. At present, you can only use the URL to watch a single event, which is very troublesome. Therefore , it is much more convenient `action_title`to add a link directly to the "event title" `main.php?op=show&action_id=活動編號`.
3. We can use `set_link($col_name)`grammar to put the link, it can be multiple groups.
4. `set_link()`For details, please refer to: [https://campus-xoops.tn.edu.tw/modules/tad\_book3/page.php?tbsn=48&tbdsn=1631](https://campus-xoops.tn.edu.tw/modules/tad_book3/page.php?tbsn=48&tbdsn=1631)
5. E.g:

   ```text
   $Model->set_link('action_title', 'main.php', ['op' => 'show', 'action_id']);
   ```

6. In this way, the activity title field in the list part will add the link we specified: ![](https://campus-xoops.tn.edu.tw/uploads/tad_book3/image/47/%E8%A8%BB%E8%A7%A3%202020-05-29%20112520.png)

