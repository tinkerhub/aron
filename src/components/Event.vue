<template>

  <div class="event">
    <span class="event-title-desc">
      <h2 class="event-name">
        {{eventName}}
      </h2>
      <p class="event-description">
        <span class="date">{{date}}</span> | <span class="about">{{about}}</span>
      </p>
    </span>  
    <p class="event-location">
      <span class="event-campus">{{campus}}</span><br>
      <span class="event-place">{{place}}</span>
    </p>
    
    <br><br>
    
    <div class="event-speaker">
      <img :src="speakerUrl" class="speaker-pic">
      <div class="speaker-info">
        <p class="speaker-name">
          {{speakerName}}
        </p>
        <span class="speaker-detail">{{speakerInfo}}</span>
      </div>
    </div>   
    
    <div class="event-skills">
      <h3 class="event-page-title">
        Skills Required
      </h3>
      <span class="ol-bullet" v-for="(skill, index) in skills">&nbsp;{{</span>
      <span class="ol-bullet">&nbsp;1&nbsp;</span><span class="ol-text">Git</span><br><br>
      <span class="ol-bullet">&nbsp;2&nbsp;</span><span class="ol-text">Python Basics</span><br><br>
      <span class="ol-bullet">&nbsp;3&nbsp;</span><span class="ol-text">Marvel Knowledge</span>
    </div>
    
  </div>

</template>

<script>
  
  module.exports = {
    name: 'Event',
    data: function() {
      return {
        speakerUrl: this.speakerAvatar
      }
    },
    props: {
      eventName: String,
      date: String,
      about: String,
      campus: String,
      place: String,
      speakerInfo: String,
      speakerName: String,
      speakerAvatar: String,
    }
  }
  
</script>

<style>

  .event {
    background-color: var(--homecolor1);
    border-radius: 5px;
    padding: 30px 40px;
    color: white;
    box-shadow:
      0 0px 2.2px rgba(0, 0, 0, 0.02),
      0 0px 5.3px rgba(0, 0, 0, 0.028),
      0 0px 10px rgba(0, 0, 0, 0.035),
      0 0px 17.9px rgba(0, 0, 0, 0.042),
      0 0px 33.4px rgba(0, 0, 0, 0.05),
      0 0px 80px rgba(0, 0, 0, 0.07)
    ;
    margin-top: 10px;
    margin-bottom: 10px;
  }
  
  .event-name {
    margin-bottom: 2px;
  }

  .event-description {
    margin-top: 0px;
  }

  .event-title-desc {
    display: inline-block;
  }
  
  .event-location {
    float: right;
  }

  .event-campus {
    font-size: 20px;
    text-align: right;
  }

  .event-place {
    font-size: 14px;
    text-align: right;
  }
  
  .speaker-pic {
    border: 4px solid white;
    width: 50px;
    height: 50px;
    border-radius: 50%;
    display: inline-block;
    vertical-align: middle;
  }

  .speaker-info {
    display: inline-block;
    margin-left: 20px;
  }

  .speaker-info {
    vertical-align: middle;
  }

  .speaker-name {
    margin-bottom: 2px;
    margin-top: 0px;
    font-weight: bold;
  }
  
  

</style>