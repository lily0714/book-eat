<script src="path/to/ripple.js"></script>
<script language="JavaScript">
Array.prototype.forEach.call(document.querySelectorAll('[data-ripple]'), function(element){
  new RippleEffect(element);
}); 
</script>
<style>
.ripple-container {
}
.ripple-container .ripple{
    background-color: rgba(255,255,255,0.4);
    animation: ripple 2s forwards cubic-bezier(0, 0, 0.2, 1);
}
@keyframes ripple {
    0% {
        transform: scale(0);
        opacity: 1;
    }
    80% {
        transform: scale(1);
    }
    100% {
        opacity: 0;
    }
}   
body{
background-color:#CEFFCE;
weight:900px;
}
.login_button{
border-radius: 10px;
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
weight:200px;
height:250px;
/*background-color:#0080FF;*/

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
      <div class="login">
      <p>登入</p>
<input type="button" value=" 登 入 " style="border-radius: 10px;" >
<input type="button" value=" 註 冊 " style="border-radius: 10px;" >
<button data-ripple class = "login_button">Click Me</button>
<button data-ripple class = "login_button">Click Me</button>
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

