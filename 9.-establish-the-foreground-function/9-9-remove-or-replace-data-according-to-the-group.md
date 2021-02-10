# 9-9 Remove or replace data according to the group

1. If a non-administrator can also see the phone number or name of the applicant, it may be a big deal... Therefore, we can see the phone number in other groups except the administrator, and the name can only see the partial name

   ```php
   case "show":
       ...略...
       $ApplyModel->disable('phone', ['index'], [1]);
       $ApplyModel->replace('uid', [], ['substr_replace' => ['this', '〇', 3, 3]], [1]);
       $ApplyModel->index();
       break;
   ```

   After adding, the administrator looks like this:  
   ![](https://campus-xoops.tn.edu.tw/uploads/tad_book3/image/47/%E7%81%AB%E7%8B%90%E6%88%AA%E5%9B%BE_2020-06-01T14-54-23.691Z.png)  
   non-administrators look like this:  
   ![](https://campus-xoops.tn.edu.tw/uploads/tad_book3/image/47/Screenshot_2020-06-01%20XOOPS%20%E8%BC%95%E9%AC%86%E6%9E%B6%20-%20%E6%B4%BB%E5%8B%95%E5%A0%B1%E5%90%8D.png)

2. Regarding the judgment group to remove a certain field:

   ```php
   $ApplyModel->disable('phone', ['index'], [1]);
   ```

   The first parameter is to `phone`prevent the field from being displayed. The  
   second parameter is to specify which functions are not displayed. At present `index`, the  
   third parameter is an exception group array, that is, which groups are not displayed in the list. The group is not hidden. Fill in \[1\] to indicate that the administrator group is not replaced, and the phone can be seen.

3. For `disable()`reference: see [API Tutorial](https://xoops.gitbook.io/jill-lazy-framework-api/3.tadmoddata-class/3-5-screen-display/3-5-6-fields-not-displayed-disable-usdcol_name)
4. Regarding the judgment group replacing the field content with a function \(rather than specifying a replacement value\):

   ```php
   $ApplyModel->replace('uid', [], ['substr_replace' => ['this', '〇', 3, 3]], [1]);
   ```

   The first parameter is for the `uid`field, because it was applied before `uid_name()`, so the field value will become the name at this time.  
   The second parameter is not filled in. It was originally the corresponding value to be filled in, but because this is not a known value \(it knows what the name of the person who signed up will be called\), so leave it blank.  
   The third parameter is the callback array, which is used to call various functions. Here, the [`substr_replace`](https://www.w3school.com.cn/php/func_string_substr_replace.asp)function is used to replace the second character of the name with 〇, and the value `this`represented `uid_name`by the  
   fourth parameter is the exception group array. , That is, which groups will not be replaced, fill in \[1\] to indicate that the administrator group will not be replaced, and you can see the full name.

