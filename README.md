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
       $(".hidebody").css({display:'block'});
        $(".loginframe").fadeIn("fast");
   });
   $("#loginclose").click(function(){
        $(".loginframe").fadeOut("fast");
        $("html").animate({opacity:'1'});
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
weight:900px;
height:100%;
position:fixed;
background-color:black;
background-image:url("https://lily0714.github.io/book-eat/遮罩.png");
opacity:0.5;
z-index:2;
left:0;
top:0;
}
.loginframe{
weight:448px;
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
#discount{
position: fixed;
bottom: 0;
right: 0;
background-color:transparent;	
}
</style>
<body>
   <div class="logo">
   <img src="http://lily0714.github.io/book-eat/bookandeat.png" weight="160" height="120">
   </div>
   <div class="hidebody"></div>
   <div class="menu">
   <p>資訊連結列:認識我們 預約座位 交通資訊 常見問題 意見回饋</p>
   </div>
   <div class="ad-login">
      <div class="k-ad">
      <p>k中廣告</p>
      </div>
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
   <img id="discount" src="https://lily0714.github.io/book-eat/包月打八折正式.png" weight="130" height="160">
   
   
</body>

