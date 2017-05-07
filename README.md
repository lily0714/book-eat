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
        $(".hidebody").css({"display":"block"});
        $(".loginframe").fadeIn("fast");
   });
   $("#loginclose").click(function(){
        $(".loginframe").fadeOut("fast");
        $(".hidebody").css({"display":"none"});
   });
});
</script>
<style>
body{
background-color:#CEFFCE;
weight:900px;
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
/*background-color:#0080FF;*/
border: 5px ridge green; 
margin-top:10px; 
margin-left:20px; 
margin-right:20px; 
margin-bottom:10px; 
padding-right:60px;
padding-bottom:-20px;
}
.hidebody{
display:none;
weight:100%;
height:100%;
position:fixed;
background-color:#000000;
z-index:2;
opacity:0.7;
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
}
#loginclose{
cursor:pointer;
}
#ylogin{
float:right;
position:relative;
right:50px;
bottom:20px;
}
form{
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
</style>
<body>
   <div class="logo">
   <img src="http://lily0714.github.io/book-eat/bookandeat.png" weight="160" height="120">
   </div>
   <div class="menu">
   <p>資訊連結列:認識我們5 預約座位4 交通資訊3 常見問題2 意見回饋1</p>
   </div>
   <div class="ad-login">
      <div class="k-ad">
      <p>k中廣告</p>
      </div>
      <div class="hidebody"></div>
      <div class="loginframe">
<img id="logintitle" src="http://lily0714.github.io/book-eat/登入框頭1.png" weight="400" height="50"><img src="http://lily0714.github.io/book-eat/登入框關閉.png" id="loginclose" weight="50" height="50">
<br>
     <form>
     <br>
     帳號:<input type="text" placeholder="請輸入帳號"><br><br>
     密碼:<input type="text" placeholder="請輸入密碼"><br>
     </form>
     <input type="button" id="ylogin" value="登 入"/>
     </div>
     <div class="login">
        <p>登入</p>
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

   
   
</body>

