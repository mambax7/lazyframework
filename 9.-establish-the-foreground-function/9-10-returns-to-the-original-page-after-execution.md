# 9-10 returns to the original page after execution

 After deleting or editing the registration, the default will return to the list instead of the original viewing single event page \( `index.php?op=show&action_id=Action ID`\), which is a bit awkward, so you can modify `header("location:xxx")`the location of \( \) after saving, updating, and deleting

```text
case "edit":
    $ApplyModel->edit($clean['apply_id']);
    break;

...略...

case "update":
    $ApplyModel->update($clean['apply_id']);
    header("location:{$from}");
    exit;

case "store":
    $ApplyModel->store();
    header("location:{$self}");
    exit;

case "destroy":
    $ApplyModel->destroy($clean['apply_id']);
    header("location:{$from}");
    exit;
```

Copy

Originally turned to `$self`, that is `$_SERVER['PHP_SELF']`\(currently located on this page, that is `index.php`\)  
switch `$form`will switch `$_SERVER['HTTP_REFERER']`, which is the position before sending, it will contain parameters, namely`index.php?op=show&action_id=1`

