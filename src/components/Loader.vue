<template>
    <div>
      <div class="loader"> 
        <img class="img" src="..\assets\ec.gif" alt="loading.." width="200"/>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: "Loader",
  };
  </script>
  
  <style>
@media only screen and (min-width: 900px) {
  .loader {
  position: fixed;
  z-index: 999;
  height: 2em;
  width: 2em;
  overflow: show;
  margin: auto;
  top: 0;
  left: 0;
  bottom: 0;
  right: 0;
}
.img {
  position: relative;
  margin: auto;
  margin-top: 20%;
} }

@media only screen and (max-width: 900px) {
  .loader {
  
  
}
.img {
  position: fixed;
  z-index: 999;
  height: 10em;
  width: 10em;
  overflow: show;
  margin:auto;
  top: 0;
  left: 0;
  bottom: 0;
  right: 0;
} 
}
    
  
  
</style>
  