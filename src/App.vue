<template>
  <div id="app">
    <header>
      <span id="left" style="font-size:30px;margin-left:15vw;cursor:pointer;">🍩</span>
      <router-link to="/about" class="right" style="margin-right:15vw;">About</router-link>
      <router-link to="/" class="right">Home</router-link>
    </header>
    
    <header>
      <a href="/events"><b class="nav-link">Events</b></a>
      <span class="line">|</span>
      <a href="/courses"><b class="nav-link">Courses</b></a>
      
      <div class="nav-right">
        <img src="https://cdn.khaleelgibran.com/img/donut.png" width="50px" class="profile-pic" style="margin-right: 20px;">
        <a href="https://tinkerhub.org"><img src="data:image/png;base64,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" class="tinkerhub" width="50px"></a>
      </div>
      
    </header>
    <router-view/>
  </div>


</template>

<style>
  
  @import url('https://fonts.googleapis.com/css2?family=IBM+Plex+Mono&display=swap');
  
  html {
    font-family: -apple-system, BlinkMacSystemFont, segoe ui, Helvetica, Arial,
      sans-serif, apple color emoji, segoe ui emoji, segoe ui symbol;
    position: relative;
    box-sizing: border-box;
    margin: 5vw;
    --primary: #0F0F23;
    --secondary: white;
    background-color: var(--primary);
    color: var(--secondary);
  }

  header {
    height: auto;
    background-color: var(--primary);
    color: var(--secondary);
    top: -3vw;
    left: 0px;
    width: 100%;
    position: absolute;
    /*   padding: 15px; */
    margin-bottom: 100px;
    box-sizing: border-box; /** add this **/
    -moz-box-sizing: border-box; /** add this **/
    -webkit-box-sizing: border-box; /** add this **/
    -ms-box-sizing: border-box; /** add this **/
    padding: 10px;
  }

  .right {
    float: right;
    display: inline-block;
    cursor: pointer;
    transition: 150ms linear;
    margin-right: 20px;
    border: 1px solid var(--secondary);
    color: var(--secondary);
    border-radius: 5px;
    padding-top: 5px;
    padding-bottom: 5px;
    padding-right: 7px;
    padding-left: 7px;
    font-family: "IBM Plex Mono", monospace;
    transition: 150ms;
  }
  
  .right:hover {
    background-color: var(--secondary);
    color: var(--primary);
    transition: 150ms;
  }

  #left {
    float: left;
    display: inline-block;
  }

  a {
    color: var(--secondary);
    border-bottom: 1px solid blue;
    text-decoration: none;
  }

</style>

