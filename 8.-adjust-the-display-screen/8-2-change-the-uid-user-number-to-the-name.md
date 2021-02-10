# 8-2 Change the uid user number to the name



1. edit`admin/main.php`
2. It can be used `uid_name()`to convert the user ID to the real name. For detailed usage, please refer to: see [API Tutorial](https://xoops.gitbook.io/jill-lazy-framework-api/3.tadmoddata-class/3-5-screen-display/3-5-4-change-uid-to-name-to-present-uid_name)
3. Application example:

   ```php
   $Model->uid_name();
   ```

4. So it will be replaced with real name 

![](../.gitbook/assets/image%20%282%29.png)

![](../.gitbook/assets/image%20%289%29.png)

