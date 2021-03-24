<template>
  <div id="app">
    <div id="top"></div>
    <div id="nav">
      <div class="nav-right">
        <img :src="user.avatar" class="avatar nav-right-el" />
        <a href="//tinkerhub.org">
          <img src="@/assets/tinkerhub.svg" class="logo nav-right-el" />
        </a>
      </div>
    </div>
    
    <router-view />
  </div>
</template>

<script>
export default {
  data: function() {
    return {
      user: {
        avatar: "https://cdn.khaleelgibran.com/donut.png"
      }
    }
  }
}
</script>

<style>

@import url('https://fonts.googleapis.com/css2?family=Fira+Code:wght@400;500;600&family=IBM+Plex+Mono&family=Inter:wght@300;400;500;800;900&family=Nunito+Sans&display=swap');

:root {
  --profilecolor1: #0E9594;
  --profilecolor2: #127475;
  --profilecolor3: #562C2C;
  --profilecolor4: #F5DFBB;
  --homecolor1: #0060FF;
  --homecolor2: #FFCD10;
  --homecolor3: #E7E7E7;
  --background: white;
  --foreground: black;
}

body {
  background-color: var(--background);
  color: var(--foreground);
  font-family: "Inter", "Roboto", "Helvetica", sans-serif;
  margin: 5vw;
}

a {
  color: inherit;
  text-decoration: none;
}

#top {
	background: var(--homecolor1);
	position: fixed;
  left: 0; right: 0;
	height: 5px;
  top: 0;
}

.nav-right {
  vertical-align: middle;
  float: right;
}

.logo {
  border-radius: 5px;
  cursor: pointer;
}

.avatar {
  height: 43px;
  width: 43px;
  border-radius: 9px;
  margin-right: 20px;
  cursor: pointer;
}

button {
  padding: 10px 20px;
  border-radius: 5px;
  font-family: "Fira Code", monospace;
  margin-top: 20px;
  margin-bottom: 20px;
  box-shadow: none;
  border: 2px solid var(--homecolor2);
  cursor: pointer;
  transition: 300ms;
  color: white;
  background-color: var(--homecolor1);
}

button:active {
  background-color: var(--homecolor2);
  color: black;
}

</style>
