# 8-3 remove part of the content



1. edit`main.php`
2. At present list is a list of all the information, but some information is actually not listed, we can use `disable('Field to be hidden', $hiddenPositionsArray)`to remove not want to display the field, you can set multiple sets. For details, please refer to: see [API Tutorial](https://xoops.gitbook.io/jill-lazy-framework-api/3.tadmoddata-class/3-5-screen-display/3-5-6-fields-not-displayed-disable-usdcol_name)
3. Both "Activity Number" `action_id`and "Activity Content" `action_content`do not need to be displayed in the list, so we set it like this:

   ```php
   $Model->disable('action_id', ['index', 'show']);
   ```

   So the list looks much cleaner  
   ![](https://campus-xoops.tn.edu.tw/uploads/tad_book3/image/47/%E7%81%AB%E7%8B%90%E6%88%AA%E5%9B%BE_2020-05-29T02-13-31.270Z.png)

4. There is no need to display the "activity number" for a single data `action_id`, so we set it like this:

   ```php
   $Model->disable('action_content', ['index']);
   ```

   So, the event number is missing, but the event content is still displayed  

![](../.gitbook/assets/image%20%2811%29.png)

