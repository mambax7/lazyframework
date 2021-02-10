# 9-13 Find specific information

1. If you log in as a general user, then go to register, and then return to the registration page after registration, you will find that the system still stupidly appears in the registration box. Generally speaking, if you have already registered, we will usually show the existing registered information, or directly show the modification form to allow users to modify the registration information. So we can modify it like this:

   ```php
   case "create":
       $apply = $ApplyModel->find(['uid']);
       if ($apply) {
           $ApplyModel->set_submit('op', 'update', '修改報名資料', 'fa-plus');
       } else {
           $ApplyModel->set_submit('op', 'store', '我要報名', 'fa-plus');
       }
       $ApplyModel->create($apply);
       break;
   ```

   Copy

   ![](https://campus-xoops.tn.edu.tw/uploads/tad_book3/image/47/%E7%81%AB%E7%8B%90%E6%88%AA%E5%9B%BE_2020-06-02T14-06-49.653Z.png)

2. For `set_submit()`the usage, please refer to the [API Tutorial](https://xoops.gitbook.io/jill-lazy-framework-api/3.tadmoddata-class/3-4-form-component/3-4-5-set-submit-button-set_submit)
3. For `find()`the usage, please refer to the [API Tutorial](https://xoops.gitbook.io/jill-lazy-framework-api/3.tadmoddata-class/3-3-data-manipulation/3-3-1-get-a-single-item-of-data-find-usdwhere_item)

