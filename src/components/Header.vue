<template>
<div class="header">
  <div class="logo"><a href="/"><img src="../assets/logo2.png"/></a></div>
  <div class="dropdown" :class="{'change':isActive}" @click="isActive = !isActive">
  <div class="bar1"></div>
  <div class="bar2"></div>
  <div class="bar3"></div>
</div>
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
  data(){
    return {isActive: false,};
  },
  name:'Header'
  
  }


</script>
<style>
@media only screen and (min-width:1200px) {


.header{
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
.dropdown {
  display:none;
}
.bar1 {
  display:none;
}
.bar2 {
  display:none;
}
.bar3 {
  display:none;
}



}
@media only screen and (min-width: 800px) and (max-width:1200px){


.header{
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
  margin: 10px 0px 0px -5%;
  display: inline-block;
  
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
 
}
.dropdown {
  display:none;
}
.bar1 {
  display:none;
}
.bar2 {
  display:none;
}
.bar3 {
  display:none;
}



}
@media only screen and (max-width: 800px) {


.header{
  display: flex;
  text-align:center;
  padding-top:20px;
  background-color:rgb(37, 37, 37);
  text-decoration:none !important ;
  font-size:150%;
  justify-content: space-between;
}
.signin{
  display:none;  
} 
a:-webkit-any-link{
    text-decoration: none !important;
    color:rgb(255, 244, 246);
}
.header-items{
  display: none;
}

.logo{
  float:left;
  margin-top:-15px;
}
}
.dropdown {
  display: inline-block;
  cursor: pointer;
}

.bar1, .bar2, .bar3 {
  width: 35px;
  height: 5px;
  background-color: #333;
  margin: 6px 0;
  transition: 0.4s;
}

.change .bar1 {
  transform: translate(0, 11px) rotate(-45deg);
}

.change .bar2 {opacity: 0;}

.change .bar3 {
  transform: translate(0, -11px) rotate(45deg);}
</style>