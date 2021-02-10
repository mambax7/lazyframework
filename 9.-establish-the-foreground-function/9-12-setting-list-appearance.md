# 9-12 Setting list appearance

1. The appearance of the table has certain preset values. If you want to adjust the appearance yourself, you can use the method of setting attributes:

   ```text
   $Model->set_attr('table', ['class' => 'table table-hover table-striped table-sm']);
   $Model->set_attr('tr1', ['class' => 'bg-warning white']);
   ...略...
   $ApplyModel->set_attr('table', ['class' => 'table table-hover table-striped']);
   $ApplyModel->set_attr('tr1', ['class' => 'bg-success white']);
   ```

   Copy

   The list on the homepage changes like this:  
   ![](https://campus-xoops.tn.edu.tw/uploads/tad_book3/image/47/%E7%81%AB%E7%8B%90%E6%88%AA%E5%9B%BE_2020-06-02T07-14-43.533Z.png)  
   The registration list on a single event page changes like this:  
   ![](https://campus-xoops.tn.edu.tw/uploads/tad_book3/image/47/%E7%81%AB%E7%8B%90%E6%88%AA%E5%9B%BE_2020-06-02T07-15-30.567Z.png)

2. `set_attr()`Usage can refer to: [https://campus-xoops.tn.edu.tw/modules/tad\_book3/page.php?tbsn=48&tbdsn=1601](https://campus-xoops.tn.edu.tw/modules/tad_book3/page.php?tbsn=48&tbdsn=1601)

