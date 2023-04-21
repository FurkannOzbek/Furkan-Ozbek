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
  }
}
    </script>

<template>

    <div > <Loader v-if="isLoading" ></Loader> fasd</div>
    <div v-if="!isLoading"><Header/></div>
    <section v-if="!isLoading" class="content">
          
         <div class="fadetext" style="animation-delay:2600ms;"><h1>Hi, my name is</h1>  </div>
         <div class="fadetext" style="animation-delay:2800ms;"><h2>Furkan Özbek</h2>  </div>
         <div class="fadetext" style="animation-delay:3000ms;"><h3>I love build websites</h3>  </div>
         <div class="fadetext" style="animation-delay:3200ms;"><p>I am a computer engineer with desire to design. Currently I am looking for a job, if you would like to contact please hit the button! </p>  </div>
         <button class="contact" style="animation-delay:3400ms;" > Contact Me</button> 
         
</section>


</template>

<style>
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
    padding: 0px;}
p{
    overflow:hidden;
}
section {
    margin: 0px auto;
    padding: 100px 0px;
    max-width: 1000px;}
.fadetext{
   animation:slide 1s forwards;
   animation-delay: 500ms;
   opacity:0;


}
@keyframes slide {
  0% { top: -100px; opacity: 0%; }
  100% { top: 0px; opacity:100%; }
}
h1{
    font-family:"SF Mono","Fira Code","Fira Mono","Roboto Mono",monospace;
    font-size:clamp(14px,5vw,16px);
    color:#64ffda;
    
}
h2{
    font-size:clamp(40px,8vw,80px);
    color:#ccd6f6;
}
h3{
    margin-top:5px;
    color:#8892b0;
    font-size: clamp(40px, 8vw, 80px);
}
p{
    margin:20px 0px 0px;
    max-width:540px;
    color:#8892b0;
}
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
   opacity:0;
}
</style>

