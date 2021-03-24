<template>
  <div id="app">
    <div id="top"></div>
    <div id="nav">
      <div class="nav-right">
        <router-link to="/me">
          <img :src="user.avatar" class="avatar nav-right-el" />
        </router-link>
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
    };
  }
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Fira+Code:wght@400;500;600&family=IBM+Plex+Mono&family=Inter:wght@300;400;500;800;900&family=Nunito+Sans&display=swap");

:root {
  --profilecolor1: #0e9594;
  --profilecolor2: #127475;
  --profilecolor3: #562c2c;
  --profilecolor4: #f5dfbb;
  --homecolor1: #0060ff;
  --homecolor2: #ffcd10;
  --homecolor3: #e7e7e7;
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
  left: 0;
  right: 0;
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
