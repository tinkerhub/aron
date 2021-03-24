<template>
  <div>
    <div class="nav">
      <span class="nav-el">Events</span>&nbsp;
      <span class="nav-el">Courses</span>
    </div>
    <div class="home-content">
      <!-- Events -->
      <Events />
    </div>
  </div>
</template>

<script>
import Events from "@/components/Events.vue";

export default {
  components: {
    Events
  }
}
</script>

<style scoped>

.nav-el {
  font-family: "Fira Code", "IBM Plex Mono", monospace;
  font-size: 25px;
  margin-right: 20px;
  transition: 200ms;
  vertical-align: middle;
}

.nav-el:hover {
  transition: 200ms;
  color: grey;
  cursor: pointer;
}

.home-content {
  margin-top: 100px;
}

</style>