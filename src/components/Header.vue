<template>
<div class="header">
<div class="logo">
  <a class="logo1" href="/"><img src="../assets/logo2.png"/></a>
    <a class="dropdown1" :class="{'change':isActive}" @click="isActive = !isActive">
  <div class="bar1"></div>
  <div class="bar2"></div>
  <div class="bar3"></div>
    </a>
    
</div>
    
  
 <a class="header-items" :class="{'header-items-none':!isActive}"><RouterLink to="/"> Home </RouterLink></a>
  <a class="header-items" :class="{'header-items-none':!isActive}"><RouterLink to="#"> About Me </RouterLink></a>
  <a class="header-items" :class="{'header-items-none':!isActive}"><RouterLink to="#"> CV </RouterLink></a>
  <a class="header-items" :class="{'header-items-none':!isActive}"><RouterLink to="#"> Contact </RouterLink></a>

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
  padding-bottom:20px;
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
  background-color: #cc4b00;
  transform-origin: bottom right;
  transition: transform 0.25s ease-out;
  margin-bottom:20px;
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
  margin: 10px -5% 0px -5%;
  display:flex;
  
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
  margin-bottom:20px;
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
.dropdown1{
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
  padding-bottom:20px;
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
  margin-bottom:20px;
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
  margin-bottom:20px;
}
.header-items:hover::after{
  transform: scaleX(1);
  transform-origin: bottom left;
}
.logo{
  float:left;
  margin-top:-15px;
 
}
.dropdown1 {
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

/*.header a{
  display:block;

}*/
.header{
  
  display: block;
  overflow:hidden;

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
  color: white;
  padding: 14px 16px;
  text-decoration: none;
  font-size: 17px;
  display: block;
  container-type:inline-size;
  text-align:center;
  
}
.header-items-none{
  display:none;
}


.logo{
float:left !important;
  
  display: inline-block;
  clear:both;
  width:100%;
  
}
.logo1{
  width:auto;
  margin-top:-15px;
  display: flex;
  clear:both;
  float:left;
  
}
.header:after{
  content:"";
  display:block;
  clear:both;
}
}
.dropdown1 {
  display: block;
  cursor: pointer;
  float:right;
  padding-right:5%;
}


.bar1, .bar2, .bar3 {
  width: 35px;
  height: 5px;
  background-color: #333;
  margin: 6px 0;
  transition: 0.4s;
  background-color:#cc4b00;
}

.change .bar1 {
  transform: translate(0, 11px) rotate(-45deg);
}

.change .bar2 {opacity: 0;}

.change .bar3 {
  transform: translate(0, -11px) rotate(45deg);}

</style>