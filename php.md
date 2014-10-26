# PHP
## 时间相关
$hSTime1 = mktime(0,0,0,4,20,2014);

$hSTime2 = mktime(0,0,0,5,12,2014);

$hSTime3 = mktime(0,0,0,5,17,2014);

$hETime3 = mktime(0,0,0,5,20,2014);

//5-5至5-11

$nowTime = time();

## 输出
<?php print $c3AssetsVersion1; ?>
<?php echo 'hello world'; ?>

## 字符串相关
* 拼接

'<link href="' . $c3AssetsServer . '/tm/act-517/' 

## 数组
$arr = array();

$arr = array('name'=> 'dlt', 'age'=>'49');

//将数据转化为字符串

$str = implode(',', $arr);

//将数组清空

$arr = array() //重新赋值

unset($arr); //数组清空

//计算数组长度

$length = count($arr);
