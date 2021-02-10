# 9-11 Set allowed groups

1. Can I sign up without logging in? Can the visitor delete the information if they enter the URL? That’s too scary, so we can set which functions allow which groups to use

   ```text
   $ApplyModel->allow(['create', 'edit', 'store', 'update', 'destroy'], [2]);
   ```

   Copy

   The first parameter is to set the function array to be checked by the group. The  
   second parameter is the allowed group array, which `1`is the administrator group, `2`the member group, and `3`the guest. `[2]`It means that as long as you have a membership group identity, you can use the aforementioned functions.

2. If there is no special setting `allow`, it means that anyone who can connect to the page can use it.
3. For `allow()`reference: [https://campus-xoops.tn.edu.tw/modules/tad\_book3/page.php?tbsn=48&tbdsn=1599](https://campus-xoops.tn.edu.tw/modules/tad_book3/page.php?tbsn=48&tbdsn=1599)
