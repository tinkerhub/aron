<template>
  <Event eventName="Pytorch" date="02/02/2021" about="Detailed description"/>
</template>

<script>
  
  import Event from '@/components/Event.vue';

  export default {
    name: 'Home',
    components: {
      Event
    }
  }
  
</script>

<style scoped>

  #donut {
    margin-top: 100px;
    height: 160px;
    border-radius: 80px;
    margin-left: auto;
    margin-right: auto;
    display: block;
  }
  
</style>