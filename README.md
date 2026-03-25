
<html>
<head>
    <title>夏令營報名表</title>
</head>

<body>
<body style="background-color:lightyellow;">

<h1 style="color:blue;">2026 夏令營報名表</h1>


<img src="camp.jpg" width="400">
<br/><br/>


<p style="color:green;">
歡迎參加我們的夏令營！請填寫以下資料完成報名。
</p>


<form method="post">

姓名：<input type="text" name="name"><br/><br/>

性別：
<input type="radio" name="gender" value="男">男
<input type="radio" name="gender" value="女">女
<br/><br/>

年齡：<input type="text" name="age"><br/><br/>

興趣：
<input type="checkbox" name="hobby[]" value="運動">運動
<input type="checkbox" name="hobby[]" value="音樂">音樂
<input type="checkbox" name="hobby[]" value="遊戲">遊戲
<br/><br/>

報名梯次：
<select name="camp">
    <option value="第一梯">第一梯</option>
    <option value="第二梯">第二梯</option>
</select>
<br/><br/>

備註：<br/>
<textarea name="note"></textarea>
<br/><br/>

<input type="submit" value="送出">

</form>

<hr/>


<?php
if(isset($_POST['name'])){
    echo "<h2>報名成功！</h2>";
    echo "姓名: " . $_POST['name'] . "<br>";
    echo "性別: " . $_POST['gender'] . "<br>";
    echo "年齡: " . $_POST['age'] . "<br>";
    
    if(isset($_POST['hobby'])){
        echo "興趣: ";
        foreach($_POST['hobby'] as $h){
            echo $h . " ";
        }
        echo "<br>";
    }

    echo "梯次: " . $_POST['camp'] . "<br>";
    echo "備註: " . $_POST['note'] . "<br>";
}
?>

<br/>


<a href="https://www.google.com" target="_blank">
更多資訊請點我
</a>

</body>
</html>
