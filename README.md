<script type='text/javascript' src='https://code.jquery.com/jquery-1.9.1.min.js'></script>
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
      
      $("#login_botton1").css({cursor:"pointer"}).click(function(){
          $(".loginframe").fadeIn("fast");
       });
       $("#loginclose").css({cursor:"pointer"}).click(function(){
          $(".loginframe").fadeOut("fast");
       });
      });
     </script>
<style>

body{
background-color:#CEFFCE;
weight:900px;
}
.login_button{
border-radius: 10px;
width:150px;
height:50px;
font-size:20px;
font-family:Microsoft JhengHei;
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
border: 5px ridge black; 
margin-top:10px; 
margin-left:20px; 
margin-right:20px; 
margin-bottom:10px; 
padding-right:60px;
padding-bottom:-20px;
}
loginframe{
weight:400px;
height:300px;
display:none;
}
ul{
list-style-type:none;
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
   <p>資訊連結列:認識我們 預約座位 交通資訊 常見問題 意見回饋</p>
   </div>
   <div class="ad-login">
      <div class="k-ad">
      <p>k中廣告</p>
      </div>
      <div class="loginframe">
     登入會員               <input id="loginclose" type="button" value="關閉"/>
     <p></p>
     <form>
     帳號:<input type="text" placeholder="請輸入帳號">
     密碼:<input type="text" placeholder="請輸入密碼">
     </form>
     <input type="button" value="登 入"/>
     </div>
      <div class="login">
      <p>登入</p>
<b>
<ul>
<li>
<input type="button" id="login_button1" class = "login_button" value=" 登 入 " />
</li>
<li>
<input type="button" id="login_button2" class = "login_button" value=" 註 冊 " onclick="window.location='https://www.instagram.com/14_shan/';" />
</li>
</ul>
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

