<?php
mysql_connect("localhost","root","webproject");//連結伺服器
mysql_select_db("webproject");//選擇資料庫
mysql_query("set names utf8");//以utf8讀取資料，讓資料可以讀取中文
$data=mysql_query("select * from webproject");//從contact資料庫中選擇所有的資料表
	//資料庫主機設定
	$db_host = "localhost";
	$db_username = "root";
	$db_password = "webproject";
	$db_name = "webproject";
	//連線資料庫
	$db_link = @new mysqli($db_host, $db_username, $db_password, $db_name);
	//錯誤處理
	if ($db_link->connect_error != "") {
		echo "資料庫連結失敗！";
	}else{
		//設定字元集與編碼
		$db_link->query("SET NAMES 'utf8'");
	}
	
session_start();
//檢查是否經過登入，若有登入則重新導向
if(isset($_SESSION["loginMember"]) && ($_SESSION["loginMember"]!="")){
	//若帳號等級為 member 則導向會員中心
	if($_SESSION["memberLevel"]=="member"){
		header("Location: member_center.php");
	//否則則導向管理中心
	}else{
		header("Location: member_admin.php");	
	}
}
//執行會員登入
if(isset($_POST["username"]) && isset($_POST["passwd"])){
	//繫結登入會員資料
	$stmt=$db_link->prepare("SELECT  id, password FROM login WHERE id=?");
	$stmt->bind_param("s", $_POST["username"]);
	$stmt->execute();
	//取出帳號密碼的值綁定結果
	$stmt->bind_result($username, $passwd);	
	$stmt->fetch();
	$stmt->close();
	//比對密碼，若登入成功則呈現登入狀態
	if(password_verify($_POST["passwd"],$passwd)){
		//計算登入次數及更新登入時間
		$stmt=$db_link->prepare("UPDATE login SET logintime=NOW(),state==”預約” WHERE id=?");
	    $stmt->bind_param("s", $username);
	    $stmt->execute();	
	header("Location: 預約系統");	
	    $stmt->close();
    }else{
		header("Location: index.php?errMsg=1");
	}
}
?>

<script type='text/javascript' src='https://code.jquery.com/jquery-3.2.1.min.js'></script>
<script type='text/javascript'>
$(document).ready(function() {
    $("#login_button1").css("color", "green");
    $("#login_button1").css("background", "white");
    $("#login_button1").mouseenter(function(){
        $("#login_button1").css("color", "white");
        $("#login_button1").css("background", "green");
    });
    $("#login_button1").mouseout(function(){
        $("#login_button1").css("color", "green");
        $("#login_button1").css("background", "white");
    });
   $("#login_button2").css("color", "green");
   $("#login_button2").css("background", "white");
   $("#login_button2").mouseenter(function(){
        $("#login_button2").css("color", "white");
        $("#login_button2").css("background", "green");
   });
   $("#login_button2").mouseout(function(){
        $("#login_button2").css("color", "green");
        $("#login_button2").css("background", "white");
   });
   /*開啟登入框loginframe*/
   $("#login_button1").click(function(){
       $(".main").css({opacity:'0.5'});
        $(".loginframe").fadeIn("fast");
   });
   $("#loginclose").click(function(){
        $(".loginframe").fadeOut("fast");
        $(".main").animate({opacity:'1'});
   });
   /*確定登入*/
   $("#ylogin").mouseenter(function(){
        $("#ylogin").css("color", "green");
        $("#ylogin").css("background", "white");
   });
   $("#ylogin").mouseout(function(){
        $("#ylogin").css("color", "white");
        $("#ylogin").css("background", "green");
   });
});
</script>
<style>
body{
background-color:#CEFFCE;
weight:900px;
height:100%;
}
.login_button{
border-radius:2px;
width:150px;
height:50px;
font-size:20px;
font-family:Microsoft JhengHei;
cursor:pointer;
position:relative;
left:30px;
z-index:1;
}
.logo{
weight:160px;
height:120px;

}
.menu{ 
weight:900px;
 
height:50px;
 
background-color:#FFFFFF;
 
}

.bigback{
weight:1000px;
height:1200px;
background-image:url("https://lily0714.github.io/book-eat/全底圖1.png");
background-repeat:no-repeat;
background-color:transparent;
position:absolute;
z-index:-1;
}
.ad-login{
weight:900px;
height:250px;
}
.k-ad{
float:left;
weight:700px;  
height:250px;
/*background-color:#424200;*/
}
.login{
float:right;
weight:200px;
height:250px;
background-image:url("https://lily0714.github.io/book-eat/登入面板1.png");
background-repeat:no-repeat;
background-size：contain contain;
/*border: 1px ridge green; */
margin-top:10px; 
margin-left:20px; 
margin-right:20px; 
margin-bottom:10px; 
padding-right:60px;
padding-bottom:-20px;
padding-top:60px;
position:relative;
z-index:1;
}
.loginframe{
weight:450px;
height:250px;
background-color:#FFFFFF;
border-radius:1px;
border-style:solid;
border-color:green;
position:fixed;
top:20%;
left:30%;
z-index:3;
display:none;
opacity:1;
}
#logintitle{
float:left;
position:relative;
left:1px;
}
#loginclose{
cursor:pointer;
float:right;
position:relative;
right:1px;
}
#ylogin{
float:right;
position:relative;
right:50px;
bottom:-10px;
color:white;
background:green;
weight:110px;
height:110px;
font-family:Microsoft JhengHei;
font-size:20px;
border-radius:2px;
cursor:pointer;
}
form{
float:left;
position:relative;
left:50px;
}
.news-good{
weight:900px;
height:450px;
}
.news{
float:left;
weight:450px;
height:450px;
/*background-color:#0080FF;*/
}
.good{
weight:450px;
height:450px;
/*background-color:#9D9D9D;*/
}
.fbad{
weight:900px;
height:300px;
background-color:#9D9D9D;
}
.link{
weight:900px;
height:100px;
background-color:#FF00FF;
}
#discount{
cursor:pointer;
position: fixed;
bottom: 0;
right: 0;
background-color:transparent;	
}
</style>
<body>
<div class="main">
   <div class="logo">
   <img src="http://lily0714.github.io/book-eat/bookandeat.png" weight="160" height="120">
   </div>
   <div class="menu"><strong>
    <a href="https://sarah862024.github.io/bookandeat/" target="_self" style="text-decoration:none;color:black;">
<nobr class="information" id="homepage">&emsp;&emsp;首  頁&nbsp;&emsp;</nobr></a>
<a href="https://sarah862024.github.io/bookandeat/about-us" target="_self" style="text-decoration:none;color:black;"> 
<nobr class="information" id="know us">&nbsp;&emsp;&emsp;認識我們&nbsp;&emsp;</nobr></a>    
<a href="https://lily0714.github.io/book-eat/預約座位" target="_self" style="text-decoration:none;color:black;"><nobr class="information" id="book seat">&nbsp;&emsp;&emsp;預約座位&nbsp;&emsp;</nobr></a>
<a href="https://sarah862024.github.io/bookandeat/traffic" target="_self" style="text-decoration:none;color:black;">
<nobr class="information" id="traffic">&nbsp;&emsp;&emsp;交通位置&nbsp;&emsp;</nobr></a>
<nobr class="information" id="QA">&nbsp;&emsp;&emsp;常見問題&nbsp;&emsp;</nobr>    
<nobr class="information" id="comment">&nbsp;&emsp;&emsp;意見回饋&nbsp;&emsp;</nobr><br> </strong>  
</div>

 <div class="bigback">
   <div class="ad-login">
      <div class="k-ad">
      <p>k中廣告123456789oiuyipo0iuyytoiiuyipu0yp98io87u75ri9i8p709po09yp9yloi;lou;poltbvkfgfkgfjjhdjfrgr</p>
      </div>
     <div class="login">
     <p></p>
<b>
<input type="button" id="login_button1" class = "login_button" value=" 登 入 " />
<br>
<br>
<input type="button" id="login_button2" class = "login_button" value=" 註 冊 "/>
</b>
     </div>
   </div>
   <p></p>
   <div class="news-good">
      <div class="news">
      <p>最新動態</p>
      </div>
      <div class="good">
      <p>傑出動態</p>
      </div>
   </div>
   <p></p>
   <div class="fbad">
   <p>食物跟參考書的廣告</p>
   </div>
   <div class="link">
   <p>重要連結</p>
   </div>
 </div>
</div>
   <img id="discount" src="https://lily0714.github.io/book-eat/包月打八折正式.png" weight="130" height="160">
   <div class="loginframe">
<img id="logintitle" src="http://lily0714.github.io/book-eat/登入框頭1.png" weight="400" height="50"><img src="http://lily0714.github.io/book-eat/登入框關閉.png" id="loginclose" weight="50" height="50">
<br>
     <form>
     <br>
     帳號:<input type="text" name="username" placeholder="請輸入帳號"><br><br>
     密碼:<input type="text" name="passwd" placeholder="請輸入密碼"><br>
     </form>
     <input type="button" id="ylogin" value="    登     入   "/>
     </div>
   
</body>

