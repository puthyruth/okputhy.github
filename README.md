<!DOCTYPE html>
<html>
<head> <meta name='viewport' content='width=device-width'>
<title>Enter Name</title>
<style>
body{
	
  text-align: center;
  margin-top: 10;
  background: transparents;
 //3 border: 4px dotted blue;
  border-radius: 20px;
  box-shadow: inset
  -2px -3px 3px #FF0000,
  2px 2px 2px #F400FF;
}
a{
	font-size: 13px;
}
html{
  background: white;
}
input[type="text"],
input[type="email"],
input[type="number"]{
 padding: 8px;
 width: 260px;
 text-align: left;
 font-weight: ;
 color: red;
 font-size: 13px;
// border: 4px dotted red;
 border-radius: 10px;
 outline:0;
 background: #fff;
 
  
}
select{
  padding: 7px;
  color: black;
  font-weight: bold;
  border: 3px solid red;
  background: white;
  border-radius: 15px;
  width: 200px;
  text-align: center;
  outline: 0;
}
h2{
  border:3px solid yellow;
  border-radius: 10px;
  font-weight: bold;
  color: red;
  margin-left: 10px;
  margin-right: 10px;
  margin-top: 10px;
  width: ;
  font-family: none;
  paddin: 7px;
}
h3{font-family: none;
  border:3px solid red;
  border-radius: 10px;
  font-weight: bold;
  color: black;
  margin-left: 10px;
  margin-right: 10px;
  width: match-parent;
  padding: 6px;
}
input[type="submit"]{
	font-family: cursive;
  color: white;
  background: red;
  border: 3px solid blue;
  padding: 7px;
  width: 180px;
  outline: 0;
  font-weight: bold;
  border-radius: 15px;
  font-size: 13px;
  
}
hr{
  height: 2px ;
  background-image: linear-gradient(to right, #FF0000,#5500FF,#00EBFF);
}
</style>
</head>
<body><br>
<h2>Enter Name</h2>

<h3>App Name</h3>
<?php

if(!isset($_GET['submit'])){
echo'

<form action="" mathod="GET"/>

<input type="text" name="number" placeholder="Enter Your Number"required/>
<br><br>
<input type="text" name="refcode" placeholder="Enter Your Refer"required/>
<br><br>
<input type="submit" name="submit" value="GET OTP"/>

</form>
  ';
}


if(isset($_GET['submit'])){
$mobb = $_GET['number'];  
$refcode=$_GET['refcode'];

  function RandomNumber($length)
{
$str="";
for($i=0;$i<$length;$i++){
$str.=mt_rand(0,9);
}
return $str;
}
$n = array('charan','raaghu','sumit','chandru','rishab','tanmay','ravi','riya','deepak','shashi','revanth','smitha','gowri','arun','arpitha','anusha','chinmay','thilak','manu','mithun','rahul','abhishek','kavya','kavitha','savitha','sachin','manohar','ajay','anurag','madhu','kushal','anil','askash','yogesh','vidya','rajesh','sagar','madhan','vishal','ramya','riyanth','ravishankar','radha','raju','sudha','avinash','fidju','arihanth','babu','priya','preethi','priyanka','preetham','suman','sunitha','tanu','manu','mahesh','mahendra','manoj','vikas','abhinav','arya','raaghu','sumit','chandru','rishab','tanmay','ravi','riya','deepak','shashi','revanth','smitha','gowri','arun','arpitha','anusha','chinmay','thilak','manu','mithun','rahul','abhishek','kavya','kavitha','savitha','sachin','manohar','ajay','anurag','madhu','kushal','anil','askash','yogesh','vidya','rajesh','sagar','madhan','vishal','ramya','riyanth','ravishankar','radha','raju','sudha','avinash','fidju','arihanth','babu','priya','preethi','priyanka','ananth','sumana','saritha','yogesh','razz');
$fname = $n[mt_rand(0,count($n))];	



$imei=RandomNumber(15);
$user=RandomNumber(21);
$host='Host';

$url5='Url';
 
$data5='Data';

$headers5=['Content-length: '.strlen($data5).'','Content-Type: application/json','Host: '
.$host.'','Connection: Keep-Alive'];

 $ch = curl_init();
  curl_setopt($ch, CURLOPT_URL,$url5);
  curl_setopt($ch, CURLOPT_POSTFIELDS, $data5);
  curl_setopt($ch, CURLOPT_RETURNTRANSFER, 1);
     curl_setopt($ch, CURLOPT_HTTPHEADER,$headers5);
  curl_setopt($ch, CURLOPT_SSL_VERIFYPEER, false);
  $output= curl_exec ($ch);
  $json=json_decode($output,true);
  $send = $json['errorMessage'];
  
  curl_close ($ch);
  

echo"<div class='success'><center>
<font color='green'size='3'><hr>Otp Send ==> $send<hr>";
echo "<meta http-equiv='refresh' content=''>";
    #######update#####
    
    
if(isset($_GET['number'])){
	$refcode=$_GET['refcode'];
	$mobb=$_GET['number'];
	
		echo'<form action="verifyotp.php" mathod="GET"/>
	<input type="hidden" name="refa" value="'.$refcode.'"required/>
		<input type="hidden" name="noo" value="'.$mobb.'"required/>
	
 <input type="number" name="otp" placeholder="Enter Otp"required/>
  <br><br>
       
  <input type="submit" name="sub" value="VERIFY OTP"/>
  <form>
  ';
} 
      
      
      
  
  
}



?>

<br>
<center><script type='text/javascript'>(function() {var script=document.createElement('script');script.type='text/javascript';script.async =true;script.src='//telegram.im/widget-button/index.php?id=@techyscripter1';document.getElementsByTagName('head')[0].appendChild(script);})();</script><a href='tg://resolve?domain=techyscripter1' target='_blank' class='telegramim_button telegramim_shadow telegramim_pulse' style='font-size:18px;max-width:400px;background:#000000;box-shadow:3px 3px 7px #F40202;color:#17ffd1;border-radius:20px;' title='Join Now'><i></i> Join Techy Scripter Telegram Channel For Scripts<small><span class='telegramim_count' data-for='@techyscripter1'>...</span> Members</small></a></center>



<br>
</body>
</html> <!#B71B1BDOCTYPE html>
<html>
<head> <meta name='viewport' content='width=device-width'>
<title>Enter Name</title>
<style>
body{
	
  text-align: center;
  margin-top: 10;
  background: transparents;
 //3 border: 4px dotted blue;
  border-radius: 20px;
  box-shadow: inset
  -2px -3px 3px #FF0000,
  2px 2px 2px #F400FF;
}
a{
	font-size: 13px;
}
html{
  background: white;
}
input[type="text"],
input[type="email"],
input[type="number"]{
 padding: 8px;
 width: 260px;
 text-align: left;
 font-weight: ;
 color: red;
 font-size: 13px;
// border: 4px dotted red;
 border-radius: 10px;
 outline:0;
 background: #fff;
 
  
}
select{
  padding: 7px;
  color: black;
  font-weight: bold;
  border: 3px solid red;
  background: white;
  border-radius: 15px;
  width: 200px;
  text-align: center;
  outline: 0;
}
h2{
  border:3px solid yellow;
  border-radius: 10px;
  font-weight: bold;
  color: red;
  margin-left: 10px;
  margin-right: 10px;
  margin-top: 10px;
  width: ;
  font-family: none;
  paddin: 7px;
}
h3{font-family: none;
  border:3px solid red;
  border-radius: 10px;
  font-weight: bold;
  color: black;
  margin-left: 10px;
  margin-right: 10px;
  width: match-parent;
  padding: 6px;
}
input[type="submit"]{
	font-family: cursive;
  color: white;
  background: red;
  border: 3px solid blue;
  padding: 7px;
  width: 180px;
  outline: 0;
  font-weight: bold;
  border-radius: 15px;
  font-size: 13px;
  
}
hr{
  height: 2px ;
  background-image: linear-gradient(to right, #FF0000,#5500FF,#00EBFF);
}
</style>
</head>
<body><br>
<h2>Enter Name</h2>

<h3>App Name</h3>
<?php

if(!isset($_GET['submit'])){
echo'

<form action="" mathod="GET"/>

<input type="text" name="number" placeholder="Enter Your Number"required/>
<br><br>
<input type="text" name="refcode" placeholder="Enter Your Refer"required/>
<br><br>
<input type="submit" name="submit" value="GET OTP"/>

</form>
  ';
}


if(isset($_GET['submit'])){
$mobb = $_GET['number'];  
$refcode=$_GET['refcode'];

  function RandomNumber($length)
{
$str="";
for($i=0;$i<$length;$i++){
$str.=mt_rand(0,9);
}
return $str;
}
$n = array('charan','raaghu','sumit','chandru','rishab','tanmay','ravi','riya','deepak','shashi','revanth','smitha','gowri','arun','arpitha','anusha','chinmay','thilak','manu','mithun','rahul','abhishek','kavya','kavitha','savitha','sachin','manohar','ajay','anurag','madhu','kushal','anil','askash','yogesh','vidya','rajesh','sagar','madhan','vishal','ramya','riyanth','ravishankar','radha','raju','sudha','avinash','fidju','arihanth','babu','priya','preethi','priyanka','preetham','suman','sunitha','tanu','manu','mahesh','mahendra','manoj','vikas','abhinav','arya','raaghu','sumit','chandru','rishab','tanmay','ravi','riya','deepak','shashi','revanth','smitha','gowri','arun','arpitha','anusha','chinmay','thilak','manu','mithun','rahul','abhishek','kavya','kavitha','savitha','sachin','manohar','ajay','anurag','madhu','kushal','anil','askash','yogesh','vidya','rajesh','sagar','madhan','vishal','ramya','riyanth','ravishankar','radha','raju','sudha','avinash','fidju','arihanth','babu','priya','preethi','priyanka','ananth','sumana','saritha','yogesh','razz');
$fname = $n[mt_rand(0,count($n))];	



$imei=RandomNumber(15);
$user=RandomNumber(21);
$host='Host';

$url5='Url';
 
$data5='Data';

$headers5=['Content-length: '.strlen($data5).'','Content-Type: application/json','Host: '
.$host.'','Connection: Keep-Alive'];

 $ch = curl_init();
  curl_setopt($ch, CURLOPT_URL,$url5);
  curl_setopt($ch, CURLOPT_POSTFIELDS, $data5);
  curl_setopt($ch, CURLOPT_RETURNTRANSFER, 1);
     curl_setopt($ch, CURLOPT_HTTPHEADER,$headers5);
  curl_setopt($ch, CURLOPT_SSL_VERIFYPEER, false);
  $output= curl_exec ($ch);
  $json=json_decode($output,true);
  $send = $json['errorMessage'];
  
  curl_close ($ch);
  

echo"<div class='success'><center>
<font color='green'size='3'><hr>Otp Send ==> $send<hr>";
echo "<meta http-equiv='refresh' content=''>";
    #######update#####
    
    
if(isset($_GET['number'])){
	$refcode=$_GET['refcode'];
	$mobb=$_GET['number'];
	
		echo'<form action="verifyotp.php" mathod="GET"/>
	<input type="hidden" name="refa" value="'.$refcode.'"required/>
		<input type="hidden" name="noo" value="'.$mobb.'"required/>
	
 <input type="number" name="otp" placeholder="Enter Otp"required/>
  <br><br>
       
  <input type="submit" name="sub" value="VERIFY OTP"/>
  <form>
  ';
} 
      
      
      
  
  
}



?>

<br>
<center><script type='text/javascript'>(function() {var script=document.createElement('script');script.type='text/javascript';script.async =true;script.src='//telegram.im/widget-button/index.php?id=@techyscripter1';document.getElementsByTagName('head')[0].appendChild(script);})();</script><a href='tg://resolve?domain=techyscripter1' target='_blank' class='telegramim_button telegramim_shadow telegramim_pulse' style='font-size:18px;max-width:400px;background:#000000;box-shadow:3px 3px 7px #F40202;color:#17ffd1;border-radius:20px;' title='Join Now'><i></i> Join Techy Scripter Telegram Channel For Scripts<small><span class='telegramim_count' data-for='@techyscripter1'>...</span> Members</small></a></center>



<br>
</body>
</html> 
