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
}
.logo{
weight:160px;
height:120px;

}
.menu{
weight:900px;
height:50px;
background-color:#AAAAFF;
}
.bigback{
weight:900px;
height:1200px;
background-image:url("https://lily0714.github.io/book-eat/全底圖.png");
background-repeat:no-repeat;
background-color:transparent;
position:relative;
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
   <div class="menu">
   <p>資訊連結列:認識我們 預約座位 交通資訊 常見問題 意見回饋</p>
   </div>
 <div class="bigback">
   <div class="ad-login">
      <div class="k-ad">
      <p>k中廣告</p>
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
     帳號:<input type="text" placeholder="請輸入帳號"><br><br>
     密碼:<input type="text" placeholder="請輸入密碼"><br>
     </form>
     <input type="button" id="ylogin" value="    登     入   "/>
     </div>
   
</body>

