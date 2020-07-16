<template>

  <span class="event-title-desc">
    <h2 class="event-name">
      {{eventName}}
    </h2>
    <p class="event-description">
      <span class="date">{{date}}</span> | <span class="about">{{about}}</span>
    </p>
  </span>  

</template>

<script>

  export default {
    name: 'EventTitleDesc',
    props: {
      eventName: String,
      date: String,
      about: String
    }
  }

</script>

<style>

  .event-name {
    margin-bottom: 2px;
  }

  .event-description {
    margin-top: 0px;
  }

  .event-title-desc {
    display: inline-block;
  }

</style>