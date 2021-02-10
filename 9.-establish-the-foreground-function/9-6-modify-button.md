# 9-6 Modify button

1. "Adding information" looks weird and it is not easy for ordinary users to understand, so it is more straightforward to change to "Register".

   ```text
   $ApplyModel->set_submit('op', 'store', 'Register', 'fa-plus');
   ```

   ![](https://campus-xoops.tn.edu.tw/uploads/tad_book3/image/47/%E7%81%AB%E7%8B%90%E6%88%AA%E5%9B%BE_2020-06-01T12-01-43.681Z.png)  

2. For `set_submit()`the usage, please refer to: see [API Tutorial](https://xoops.gitbook.io/jill-lazy-framework-api/3.tadmoddata-class/3-4-form-component/3-4-5-set-submit-button-set_submit)
3. After clicking "I want to sign up", from the database, I did see that a record was added 

![](../.gitbook/assets/image%20%287%29.png)

