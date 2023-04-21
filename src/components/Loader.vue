<template>
    <div>
      <div class="loader"> 
        <img class="img" src="..\assets\wd6r6HlME.gif" alt="loading.." width="200"/>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: "Loader",
  };
  </script>
  
  <style>
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
}
</style>
  