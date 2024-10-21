<template>
  <header id=header1 class="header1">
  <div class="logo">
    <a class="logo1" href="/"><img src=""/></a>
      <a class="dropdown1" :class="{'change':isActive}" @click="isActive = !isActive">
    <div class="bar1"></div>
    <div class="bar2"></div>
    <div class="bar3"></div>
      </a>
  </div>
  <div class="header-item">
    <ol>
      <a href="#About"><li class="header-items" :class="{'header-items-none':!isActive}" style="animation-delay:300ms;">About Me </li></a>
      <a href="#jobs"><li class="header-items" :class="{'header-items-none':!isActive}" style="animation-delay:600ms;">Experience </li></a>
      <a href="#pskills"><li class="header-items" :class="{'header-items-none':!isActive}" style="animation-delay:900ms;">Skills</li></a>
      <a href="#contact1"><li class="header-items" :class="{'header-items-none':!isActive}" style="animation-delay:1200ms;">Contact </li></a>
      
      <a class="cv" :class="{'cv-none':!isActive}" style="animation-delay:1500ms;" href="\src\assets\resume.pdf"  target=”_blank”>Resume</a>
      <a class="cv" :class="{'cv-none':!isActive}" style="animation-delay:1800ms;" href="\src\assets\vurdering.pdf"  target=”_blank”>Vurdering</a>
      <a class="cv" :class="{'cv-none':!isActive}" style="animation-delay:2000ms;" href="\src\assets\soft.pdf"  target=”_blank”>Soft Skills</a>
      
      
  </ol>
  
  </div>
</header>
  
  </template>
  
  <script>
  export default{
    data(){
     
      return {
             
              isActive: false,
              isScDown:false,
              startY:0,
              ScrollPosition:null,};
    },
    methods: {
    handleScroll() {
      let d = document.getElementById("header1")
      let scrollY = window.scrollY
      if (scrollY > this.startY){
        d.className =("header1down")
      }
       if (scrollY < this.startY){
        d.className= ("header1up")
      }
      if (scrollY === 0){
        d.className= ("header1")
      }
     
      this.startY = scrollY;
    }
    
  },

  mounted() {
    window.addEventListener('scroll', this.handleScroll);
  },
    name:'Header'
    
    }
  
  
  </script>
  <style>
  @media only screen and (min-width:900px) {
  
    body {
    counter-reset: item section section2; /* Set a counter named 'item', and its initial value is 0. */
    display: block;
  }
  header{
    height:70px;
    display: flex;
    position: inherit;
    z-index:1000;
    
    
  }
  .cv:hover {
    background-color:#64ffda;
    
    color:rgb(44, 42, 42);
    border: 1px solid #3b3d3d;
    transition:ease-in 0.5s;
  }
  .cv a:hover {
    background-color:#64ffda;
    
    color:rgb(44, 42, 42);
    border: 1px solid #3b3d3d;
    transition:ease-in 0.5s;
  }
  .header1{
    
    padding-top:10px;
    top:0;
    align-items: center;
    width:100%;
    display: block;
    text-align:center;
    position:fixed;
    background-color:#212529;
    text-decoration:none !important ;
    scroll-behavior: smooth;
    justify-content: space-between;
     transition:all 0.25s cubic-bezier(0.645,0.045,0.355,1);
   
    
  }
  .header1up{
    
    top:0;
    width:100%;
    display: block;
    text-align:center;
    position:fixed;
    background-color:#212529ef;
    text-decoration:none !important ;
    scroll-behavior: smooth;
    justify-content: space-between;
    transition:all 0.25s cubic-bezier(0.645,0.045,0.355,1);
    box-shadow: 0 10px 30px -10px rgba(2,12,27,0.7);;
    transform: translateY(0px);
    
    
  }
  .header1down{
    align-items:center;
    top:0;
    scroll-behavior: smooth;
    width:100%;
    display: block;
    text-align:center;
    position:fixed;
    background-color:#212529;
    text-decoration:none !important ;
    padding-bottom:20px;
    justify-content: space-between;
    transform: translateY(-120px);
    transition:all 0.25s cubic-bezier(0.645,0.045,0.355,1);
    
    
  }
 .header1down ol li{
 padding:15px;
 margin-top:10px;
 }
  .header1 ol li {
    padding:15px;
    transition:all 0.25s cubic-bezier(0.645,0.045,0.355,1);
    
    
    
  }
  .header1up ol li {
    padding:15px;
    margin-top:10px;
    
  }
  div.header-item{
    position:flex;
    float:right;
    padding-right:3%;
    
  }
  .cv {
    transition-timing-function: linear;
    transition-timing-function: cubic-bezier(0, 0, 1, 1);
      transition: 0.5s;
      margin:0 5px 0 5px;
      align-items: center;
      color: #64ffda;
      background-color: transparent;
      border: 1px solid #66ffdb;
      border-radius: 4px;
      padding: 0.75rem 0.75rem;
      font-family:"SF Mono","Fira Code","Fira Mono","Roboto Mono",monospace;
      line-height: 1;
      text-decoration: none;
      cursor: pointer;
      animation:slide 1s forwards;
      animation-delay: 500ms;
      
      font-size:13px;
      opacity:0;
  }
  button:hover{
    background-color:#64ffda;
    
    color:rgb(44, 42, 42);
    border: 1px solid #3b3d3d;
    transition:ease-in 0.5s;
   }
  a:-webkit-any-link{
      text-decoration: none !important;
      color:rgb(255, 244, 246);
  }
  .header-items{
    font-family: "SF Mono","Fira Code","Fira Mono","Roboto Mono",monospace;
    font-size:13px;
    display:inline-block;
    margin-top:20px;
    animation:slide 1s forwards;
   animation-delay: 500ms;
   opacity:0;
    }
    
  
   .header-items::before {
    counter-increment: item;
    content: "0" counter(item) ".";
    color:#64ffda;
    text-align: right;
    font-size:12px;
    
    padding-top:4px;
   }
  .header-items::after{
    content: '';
    position:absolute;
    width: 100%;
    transform: scaleX(0);
    height: 2px;
    bottom: 0;
    left: 0;
    background-color: #66ffdb;
    transform-origin: bottom right;
    transition: transform 0.25s ease-out;
    
  }
  .header-items:hover{
    
    color:#66ffdb
  }
  .header-items:hover::after{
    transform: scaleX(1);
    transform-origin: bottom left;
  }
  .logo{
    float:left;
    
  
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

  @media only screen and (max-width: 900px) {
  
  .header a{
    display:block;
    
  
  }
  
  .header1{
   
    align-items: center;
    display:block;
    overflow:hidden;
    padding-bottom:20px;
    padding-top:20px;
    background-color: #212529;
    text-decoration:none !important ;
    font-size:150%;
    justify-content: space-between;
    
  }
  .header1up{
    display:none;
    
    
  }
  .header1down{
    align-items: center;
    display:block;
    overflow:hidden;
    padding-bottom:20px;
    padding-top:20px;
    background-color: #212529;
    text-decoration:none !important ;
    font-size:150%;
    justify-content: space-between;
    
  }
  .cv{
    color: #64ffda;
      background-color: transparent;
      border: 1px solid #66ffdb;
      border-radius: 4px;
      padding: 0.75rem 1rem;
      font-family:"SF Mono","Fira Code","Fira Mono","Roboto Mono",monospace;
      line-height: 1;
      text-decoration: none;
      cursor: pointer;
      
      transition: all 0.25s cubic-bezier(0.645,0.045,0.355,1);;
    
      font-size:13px;
  } 
  a:-webkit-any-link{
      text-decoration: none !important;
      color:rgb(255, 244, 246);
  }
 

  .header-items{
    color: #66ffdb;
    padding: 14px 16px;
    text-decoration: none;
    font-size: 17px;
    display:block;
    container-type:inline-size;
    text-align:center;
    margin-bottom:5px;
    
    
  }
  .header-items-none{
    display:none;
    
  }
  .header-item{
    color: white;
    padding: 14px 16px;
    text-decoration: none;
    font-size: 17px;
   
    container-type:inline-size;
    text-align:center;
    transform: translateY(0vw);
    
    
  }
  .header-item-none{
    display:none;
    transform: translateY(100vw);
  }
  .cv-none {
    display:none;
  }
  
  
  .logo{
  float:left !important;
    
    display: inline-block;
    clear:both;
    width:100%;
    
  }
  .logo1{
   
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
    background-color:#64ffda;
  }
  
  .change .bar1 {
    transform: translate(0, 11px) rotate(-45deg);
  }
  
  .change .bar2 {opacity: 0;}
  
  .change .bar3 {
    transform: translate(0, -11px) rotate(45deg);}
  
    a:-webkit-any-link:hover {
      
      transition-delay: 0s;
      color:66ffdb;
    }
   
  </style>