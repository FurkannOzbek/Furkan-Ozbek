<template>
<div class="navbar-container">
  <div class="logo"><a href="/"><img src="../assets/logo2.png"/></a></div>
  <div class="header-items"><RouterLink to="/"> Home </RouterLink></div>
  <div class="header-items"><RouterLink to="#"> About Me </RouterLink></div>
  <div class="header-items"><RouterLink to="#"> CV </RouterLink></div>
  <div class="header-items"><RouterLink to="#"> Contact </RouterLink></div>
  
     <div class="signin">
        <div class="sign-in" style="margin-right:30px"><RouterLink to="#"> Log In</RouterLink></div>
        <div class="sign-in"><RouterLink to="#" > Register</RouterLink></div>
      
    </div>
  </div>
</template>

<script>
export default{
  name:'Header'
}</script>

<style>
.navbar-container{
  display: flex;
  text-align:center;
  padding-top:20px;
  background-color:rgb(37, 37, 37);
  text-decoration:none !important ;
  font-size:150%;
  justify-content: space-between;
}

.signin{
  display:flex;
  float:right;
  margin-right:20px;
  text-decoration:none !important ;
  font-size: 20px;
  padding-top:10px;
  font-family:'Times New Roman', Times, serif;
  
} 
.sign-in::after{
  content: '';
  position:absolute;
  width: 100%;
  transform: scaleX(0);
  height: 2px;
  bottom: 0;
  left: 0;
  background-color: #ca4a00;
  transform-origin: bottom right;
  transition: transform 0.25s ease-out;
  margin-bottom:30px;
}
.sign-in:hover::after{
  transform: scaleX(1);
  transform-origin: bottom left;
}


a:-webkit-any-link{
    text-decoration: none !important;
    color:rgb(255, 244, 246);
}
.header-items{
  font-family:'Times New Roman', Times, serif;
  font-size:20px;
  margin: 10px -10% 0px -5%;
  display: inline-block;
  position: relative;
  color: #006091;
 
}
.header-items::after{
  content: '';
  position:absolute;
  width: 100%;
  transform: scaleX(0);
  height: 2px;
  bottom: 0;
  left: 0;
  background-color: #ca4a00;
  transform-origin: bottom right;
  transition: transform 0.25s ease-out;
  margin-bottom:30px;
}
.header-items:hover::after{
  transform: scaleX(1);
  transform-origin: bottom left;
}
.logo{
  float:left;
  margin-top:-15px;
  margin-right:20%;
}






</style>