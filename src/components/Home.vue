<script>
import Header from './Header.vue'
import Loader from './Loader.vue'


export default{
    name:'Home',
    data() {
        return {
            isLoading:true,
        };
    },
    components: {
        Header,
        Loader,
    },
    mounted() {
    setTimeout(() => {
      this.isLoading = false;
    }, 1500);
    window.addEventListener('scroll', this.handleScroll);
  },
  methods: {
    handleScroll() {
      var e = document.getElementById("About")
      var f = document.getElementById("jobs")
      var g = document.getElementById("pskills")
      
      var scrollY = window.scrollY
      if (scrollY > 300) {
        e.className= ("Aboutvis")
      }
      if (scrollY > 800){
        f.className= ("jobsvis")
      }
      if (scrollY > 1600){
        g.className= ("skillsvis")
      }
     
    },
     asd(tabnumber){
        var i;
        var x = document.getElementsByClassName("tab");
        for (i = 0; i < x.length; i++) {
        x[i].style.display = "none";
      
  }
  
        //reseting all the tabs after each function usage 
        var tab1 = document.getElementById("tab1")
        var tab2 = document.getElementById("tab2")
        var tab3 = document.getElementById("tab3")
        tab1.className = "jobtabothers";
        tab2.className = "jobtabothers";
        tab3.className = "jobtabothers";
        var a = event.currentTarget
        
        if (a.className = "jobtabothers"){
            a.className = "jobtabselected"
          document.getElementById("followline").className=("followline"+a.id)
           

            
      }
      document.getElementById(tabnumber).style.display = "block" ;
      document.getElementById(tabnumber).style.transition = "all 0.25s cubic-bezier(0.645,0.045,0.355,1);"
     }
    
  },
}
    </script>

<template>
   
    <div > <Loader v-if="isLoading" ></Loader></div>
    <div v-if="!isLoading"><Header/></div>
    <main>
    <section v-if="!isLoading" class="content">
          
         <div class="fadetext" style="animation-delay:2600ms;"><h1>Hi, my name is</h1>  </div>
         <div class="fadetext" style="animation-delay:2800ms;"><h2>Furkan Özbek</h2>  </div>
         <div class="fadetext" style="animation-delay:3000ms;"><h3>I love build websites</h3>  </div>
         <div class="fadetext" style="animation-delay:3200ms;"><p>I am a computer engineer with desire to design. Currently I am looking for a job, if you would like to contact please hit the button! </p>  </div>
         <button class="contact" style="animation-delay:3400ms;" > Contact Me</button> 
         
</section >

<section v-if="!isLoading" id="About" class="About"  > 
    <h2 class="numberheading"> About Me</h2>
    <div class="inner">
        <div>
            
 <p> Hello, My name is Furkan and I really love design websites. My interest in web development started back in 2014 when I have designed some few website for the people who is close to me. At those times I were using 
    wordpress ready themes and with custom css I were designing. Then I have met with Javascript and Vue.js and started to code my websites from scracth.
 </p>
 <p> 
    Here are some methods I am familiar with:
 </p>

<ul class="skills1">
    <li> HTML</li>
    <li> CSS</li>
    <li> Javascript</li>
    <li> Vue.js</li>
   
</ul>
</div>
<div> <img class="pic" src="../assets/asdf.jpg"></div>
</div>
</section>
<section id="jobs" class="jobs">
    <h2 class="numberheading"> Work Experience</h2>
    <div class="inner">
        <div id="tablist" class="joblist">
            <button id="tab1"    class="jobtabothers" v-on:click="asd('tab11')"> <span> C2Tech </span></button>
            <button id="tab2"    class="jobtabothers"   v-on:click="asd('tab22')">    <span > Alya Boutique Hotel </span></button>
            <button id="tab3"    class="jobtabothers"   v-on:click="asd('tab33')">   <span> KFC </span></button>
            <div id="followline" class="followlinetab1"></div>
            
        </div>
        <div class="worktext">
<div id="tab11" class="tab"> <h3> 
    <span>Technical Sales Engineer</span> 
    <span class="company"> @ C2Tech </span>
</h3>
<p class="distance">
    Date 2131 - 1200
</p> 
<div>
    <ul>
        <li>It is a long established fact that a reader will be distracted by the readable content of a page when looking at its layout. The point of using Lorem Ipsum is that it has a more-or-less normal distribution of letters, as opposed to using 'Content here, content here', making it look like readable English. Many desktop publishing</li>
        <li>Lorem Ipsum is simply rised in</li>
        <li>Contrary to popular belief, Lorem Ipsum is not simply random text. It has roots in a piece of classical Latin literature from 45 BC</li>
        <li>as</li>
    </ul> </div></div>
    <div id="tab22" class="tab" style="display:none"> <h3> 
    <span>Internal IT Support</span> 
    <span class="company"> @ Alya Boutique Hotel </span>
</h3>
<p class="distance">
    Date 2131 - 1200
</p> 
<div>
    <ul>
        <li>It is a long established fact that a reader will be distracted by the readable content of a page when looking at its layout. The point of using Lorem Ipsum is that it has a more-or-less normal distribution of letters, as opposed to using 'Content here, content here', making it look like readable English. Many desktop publishing</li>
        <li>Lorem Ipsum is simply rised in</li>
        <li>Contrary to popular belief, Lorem Ipsum is not simply random text. It has roots in a piece of classical Latin literature from 45 BC</li>
        <li>as</li>
    </ul> </div></div>
    <div id="tab33" class="tab" style="display:none"> <h3> 
    <span> Shiftleader </span> 
    <span class="company"> @ KFC </span>
</h3>

<p class="distance">
    Date 2131 - 1200
</p> 
<div>
    <ul>
        <li>It is a long established fact that a reader will be distracted by the readable content of a page when looking at its layout. The point of using Lorem Ipsum is that it has a more-or-less normal distribution of letters, as opposed to using 'Content here, content here', making it look like readable English. Many desktop publishing</li>
        <li>Lorem Ipsum is simply rised in</li>
        <li>Contrary to popular belief, Lorem Ipsum is not simply random text. It has roots in a piece of classical Latin literature from 45 BC</li>
        <li>as</li>
    </ul> </div></div>

</div>
    </div>

</section>
<section v-if="!isLoading" id="pskills" class="pskills"  > 
    <h2 class="numberheading"> My Skills</h2>
    <div class="inner">
        <div>
            <h1 style="padding-top:50px;font-size: 30px;"> Technology </h1>
 <p class="prskills"> I have been always interested with technology especially technology in computer area. Hereby some of my skills and interests about technology
 </p>


</div>

<div id="graphs" class="graphs"> 
    <li class="graphsli"><h3> HTML and CSS </h3> <span class="bar"><span class="html"></span></span> </li>
    <li class="graphsli"><h3> Javascript and Vue </h3> <span class="bar"><span class="java"></span></span> </li>
    <li class="graphsli"><h3> MS Office and OS </h3> <span class="bar"><span class="ms"></span></span> </li>
    <li class="graphsli"><h3> Network </h3> <span class="bar"><span class="net"></span></span> </li>

</div>

</div>
<div class="inner" style="padding-top:150px;padding-right:50px;">
        

<div id="graphs" class="graphs"> 
    <li class="graphsli"><h3> English </h3> <span class="bar"><span class="eng"></span></span> </li>
    <li class="graphsli"><h3> Danish </h3> <span class="bar"><span class="dan"></span></span> </li>
    <li class="graphsli"><h3> Turkish</h3> <span class="bar"><span class="tr"></span></span> </li>
    

</div>
<div style="padding-left:50px;">
            <h1 style="padding-top:50px;font-size: 30px;"> Language </h1>
 <p class="prskills">Eventho my mother language is Turkish I can speak well English and I am currently learning Danish.
 </p>


</div>
</div>

</section>
<section v-if="!isLoading" id="contact1" class="contact1">
<div><h4 class="numberheadinglast"> Contact </h4>
<p class="lasttext"> Although I’m not currently looking for any new opportunities, my inbox is always open. Whether you have a question or just want to say hi, I’ll try my best to get back to you!</p>
<button class="contact" style="animation-delay:3400ms;" > Contact Me</button> 
</div></section>

</main>
</template>

<style>
.worktext{
    max-width:500px;
}
.content{
    background-color: #212529;
    display: flex;
    -webkit-box-pack: center;
    justify-content: center;
    -webkit-box-align: center;
    flex-direction: column;
    align-items: flex-start;
    min-height: 100vh;
    height: 100vh;
    padding: 0px;max-width:100%;overflow: hidden;}
    .contact1{
       
        text-align: center;
    }
    
    .lasttext{
        text-align: center;
        margin-right:auto;
        margin-left:auto;
    }
p{
    
    overflow:hidden;}
section {
    margin: 60px auto;
    padding: 100px 0px;
    max-width: 1000px;}
.fadetext{
   animation:slide 1s forwards;
   animation-delay: 500ms;
   opacity:0;}
@keyframes slide {
  0% { top: -100px; opacity: 0%; }
  100% { top: 0px; opacity:100%; }}
h1{
    font-family:"SF Mono","Fira Code","Fira Mono","Roboto Mono",monospace;
    font-size:clamp(14px,5vw,16px);
    color:#64ffda;}
h2{
    font-size:clamp(40px,8vw,80px);
    color:#ccd6f6;}
h3{
    margin-top:5px;
    color:#8892b0;
    font-size: clamp(40px, 8vw, 80px);}
p{
    margin:20px 0px 0px;
    max-width:540px;
    color:#8892b0;}
.contact{
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
   margin-top:20px;
      font-size:13px;
      transition: all 0.25s cubic-bezier(0.645,0.045,0.355,1);
      animation:slide 1s forwards;
   animation-delay: 500ms;
   opacity:0;}
.About{
    opacity:0;}
.Aboutvis{
    
    padding-left:100px;
    visibility: visible; 
    opacity: 1; 
    transform: matrix3d(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1); 
    transition: opacity 0.5s cubic-bezier(0.645, 0.045, 0.355, 1) 0.2s, transform 0.5s cubic-bezier(0.645, 0.045, 0.355, 1) 0.2s;}
.pskills{
    opacity:0;}
.skillsvis{
    
    padding-left:100px;
    visibility: visible; 
    opacity: 1; 
    transform: matrix3d(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1); 
    transition: opacity 0.5s cubic-bezier(0.645, 0.045, 0.355, 1) 0.2s, transform 0.5s cubic-bezier(0.645, 0.045, 0.355, 1) 0.2s;}
.jobs{
    opacity:0;}
.jobsvis{
    
    padding-left:200px;
    visibility: visible; 
    opacity: 1; 
    transform: matrix3d(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1); 
    transition: opacity 0.5s cubic-bezier(0.645, 0.045, 0.355, 1) 0.2s, transform 0.5s cubic-bezier(0.645, 0.045, 0.355, 1) 0.2s;}
.numberheading {
    display: flex;
    -webkit-box-align: center;
    align-items: center;
    position: relative;
    margin: 10px 0px 40px;
    width: 100%;
    font-size: clamp(26px,5vw,32px);
    white-space: nowrap;
    max-width:900px;}
.numberheading::before {
    position: relative;
    top:7px;
    counter-increment: section 1;
    content: "0" counter(section) ".";
    margin-right: 10px;
    color: #64ffda;
    font-family: "SF Mono","Fira Code","Fira Mono","Roboto Mono",monospace;
    font-size: clamp(16px,3vw,20px);
    font-weight: 400;}
    .numberheadinglast {
    
    -webkit-box-align: center;
    align-items: center;
    position: relative;
    margin: 10px 0px 40px;
    width: 100%;
    font-size: clamp(26px,5vw,32px);
    white-space: nowrap;
    }
    .numberheadinglast::before {
    position: relative;
    top:0px;
    counter-increment: section 1;
    content: "0" counter(section) ".";
    
    color: #64ffda;
    font-family: "SF Mono","Fira Code","Fira Mono","Roboto Mono",monospace;
    font-size: clamp(16px,3vw,20px);
    font-weight: 400;}
.numberheading::after {
    content: "";
    display: block;
    position: relative;
 
    width: 300px;
    height: 1px;
    margin-left: 20px;
    background-color: #66ffdb21;}   
main {
    margin: 0px auto;
    width: 100%;
    max-width: 1600px;
    min-height: 100vh;
    padding: 0px 150px;}
ul.skills1 {
    display:grid;
    grid-template-columns: repeat(2, minmax(140px, 200px));
    gap:0px 10px;
    padding:0px;
    margin:20px 0px 0px;
    overflow:hidden;
    list-style:none;}
ul.skills1 li::before {
    content: "▹";
    position: absolute;
    left: 0px;
    color: #64ffda;
    font-size: 14px;
    line-height: 12px;
    margin-top:7px;}
ul.skills1 li{
    position:relative;
    padding-left:20px;
    padding-top:15px;}
.inner{
    display: flex;
    grid-template-columns: 3fr 2fr;
    gap: 50px;
}
.pic{

    border-radius:4px;
    max-height: 50%;
    max-width:50%;}
.jobtabselected{
        text-decoration: none;
    text-decoration-skip-ink: auto;
    position: relative;
    transition:  all 0.25s cubic-bezier(0.645,0.045,0.355,1);
    display: flex;
    -webkit-box-align: center;
    align-items: center;
    width: 100%;
    height: 42px;
    padding: 0px 20px 2px;
    border-left: 2px solid #64ffda;
    background-color: transparent;
    color: #64ffda;;
    font-family: "SF Mono","Fira Code","Fira Mono","Roboto Mono",monospace;
    font-size: 13px;
    text-align: left;
    white-space: nowrap; }
button.jobtabselected{
    cursor: pointer;
    border: 0px;
    border-radius: 0px;}
.jobtabothers{
    text-decoration: none;
    text-decoration-skip-ink: auto;
    position: relative;
    transition: all 0.25s cubic-bezier(0.645,0.045,0.355,1);
    display: flex;
    -webkit-box-align: center;
    align-items: center;
    width: 100%;
    height: 42px;
    padding: 0px 20px 2px;
    border-left: 2px solid #4d565fa9 !important;
    background-color: transparent;
    color: #8892b0;
    font-family: "SF Mono","Fira Code","Fira Mono","Roboto Mono",monospace;
    font-size: 13px;
    text-align: left;
    white-space: nowrap;}
button.jobtabothers {
    cursor: pointer;
    border: 0px;
    border-radius: 0px;}
button.jobtabothers:hover {
    background-color:#404850;
    cursor: pointer;
    color: #64ffda;
    border: 0px;
    border-radius: 0px;}
.followlinetab1{
    
    position: absolute;
    top: 0px;
    left: 0px;
    z-index: 10;
    width: 2px;
    height: 42px;
    border-radius: 4px;
    background: #64ffda;
    transform: translateY(calc(0 * 42px));
    transition: transform 0.25s cubic-bezier(0.645, 0.045, 0.355, 1) 0.1s;}    
.followlinetab2{
    
    position: absolute;
    top: 0px;
    left: 0px;
    z-index: 10;
    width: 2px;
    height: 42px;
    border-radius: 4px;
    background: #64ffda;
    transform: translateY(calc(1 * 42px));
    transition: transform 0.25s cubic-bezier(0.645, 0.045, 0.355, 1) 0.1s;}    
.followlinetab3{
    
    position: absolute;
    top: 0px;
    left: 0px;
    z-index: 10;
    width: 2px;
    height: 42px;
    border-radius: 4px;
    background: #64ffda;
    transform: translateY(calc(2 * 42px));
    transition: transform 0.25s cubic-bezier(0.645, 0.045, 0.355, 1) 0.1s;}    
.joblist{
    position: relative;
    z-index: 3;
    width: max-content;
    padding: 0px;
    margin: 0px;
    list-style: none;}
h3 {
    font-size:22px;
    display:block;
    color:#ccd6f6;}
p.distance{
    margin-bottom:25px;
    color:white;
    font-size:13px;
    font-family:"SF Mono","Fira Code","Fira Mono","Roboto Mono",monospace;}
ul {list-style:none;
padding-left:0px !important;}
ul li{
    position: relative;
    padding-left: 30px;
    margin-bottom: 10px;}

ul li::before{
    content: "▹";
    position: absolute;
    left: 0px;
    color: #66ffdb;;}
.company{
    color:#64ffda;}
button:focus {
    outline:0px ; }
.tab{
   animation:slide2 0.5s forwards;
   animation-delay: 0ms;
   opacity:0;}
@keyframes slide2 {
  0% {  opacity: 0%; }
  100% { opacity:100%; }}
p.prskills{
    margin-top:50px;
    max-width: 350px;
}
li.graphsli{
    list-style-type: none;
	font-family: sans-serif;
}
.graphs{ /*style the text*/
    box-sizing:unset !important;
	width: 300px;
	margin: 10px 10px;
	color: #fff;
}
.graphs li{ /*set margin of li*/
	margin: 20px 0;
}
.bar{ /*style the bar*/
	background-color: #353b48;
	display: block;
	height: 2px;
	border: 1px solid rgba(0,0,0,0.3);
	border-radius: 3px;
	overflow: hidden;
	box-shadow: 0 0 10px #64ffdb98;
}

.bar span{ /*style the span tag*/
	height: 2px;
	float: left;
	background-color: #64ffda;
  
}
.html{ /*set skills and animation of html*/
   
	width: 80%;
	animation:html 5s;
}

.java{ /*set skills and animation of css*/
	width: 53%;
	animation: java 5s;
}

.ms{ /*set skills and animation of javascript*/
	width: 70%;
	animation: ms 5s;
}

.net{ /*set skills and animation of jquery*/
	width: 60%;
	animation: net 5s;
}
.eng{
    width:85%;
    animation:eng 5s;
}
.dan{
    width:35%;
    animation:dan 5s;
}
.tr{
    width:100%;
    animation:tr 5s;
}

@keyframes html{ /*animate html skills*/
	0%{
		width: 0%;
	}

	100%{
		width: 70%;
	}
}

@keyframes java{ /*animate css skills*/
	0%{
		width: 0%;
	}

	100%{
		width: 53%;
	}
}

@keyframes ms{ /*animate javascript skills*/
	0%{
		width: 0%;
	}

	100%{
		width: 70%;
	}
}

@keyframes net{ /*animate jquery skills*/
	0%{
		width: 0%;
	}

	100%{
		width: 60%;
	}

    }
    @keyframes eng{ /*animate jquery skills*/
	0%{
		width: 0%;
	}

	100%{
		width: 85%;
	}

    }
    @keyframes dan{ /*animate jquery skills*/
	0%{
		width: 0%;
	}

	100%{
		width: 35%;
	}

    }
    @keyframes tr{ /*animate jquery skills*/
	0%{
		width: 0%;
	}

	100%{
		width: 100%;
	}

    }
    *, ::after, ::before {
    box-sizing: inherit;
}
</style>

