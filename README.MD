# Victoria Tran 
# CWID: 889773024
# CS 349-01 MIDTERM 

---------------------------------------------------


# Question 1
```html

<!DOCTYPE html>
<!--VICTORIA TRAN
  CS 349-01
  MIDTERM CODING QUESTION 1
-->
<html>
<head>
  <meta charset="utf-8">
  <title> FORM</title>
  </head>
  <body>

    <form>

      FIRST NAME: <input type ="text" name ="FIRST NAME: " autofocus required placeholder="">
      LAST NAME: <input type ="text" name ="LAST NAME: "required  placeholder="">
      EMAIL: <input type ="text" name ="LAST NAME: "required  placeholder="">
      MAJOR:

      <!--RADIO BUTTONS-->
      <label for="CS">
        <input type="radio" name="CS" checked>CS
      </label>

      <label for="CSCE">
        <input type="radio" name="CSCE">CSCE
      </label>

      <label for="MATH">
        <input type="radio" name="MATH"> MATH
      </label>

    <!--BUTTONs-->
      <button type="submit"name="submit">Submit </button>
      <button type="reset"name="reset"> Reset </button>

     </form>
    </body>

  </html>


```

# Question 2
```php
<?php
$dbServerName = "hello.com";
$dbUsername = "hello";
$dbPassword = "password";
$dbName = "databaseExample";

$conn = new mysqli($dbServerName, $dbUsername, $dbPassword, $dbName);

if ($conn->connect_error) {
//ERROR CHECK
    die("Failed to Connect: " . $conn->connect_error);
}
echo "Connected!";
?>

```
# Question 3
```php
$db_userid = $row->admin_id;
$db_password = $row→admin_password;
$encryptpasswd = sha1($userPasswd); 
$db_name = $row->admin_name;

if ($db_userid != $userid || $db_password != $encryptpasswd) {
 
 // ***THE MISSING CODE: add record to admin table ***
 $query = "INSERT INTO administrator(admin_id, admin_password, admin_name)
 VALUES('$userid', '$encryptpasswd', '$name')";
 
 $result = mysqli_query($connection, $query);
 
 if (!$result) {
 echo ("Insert to administrator failed. ". mysqli_error($connection));
 exit();
 }
}

```
