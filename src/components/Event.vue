<template>
    <div class="event">
        <p class="event-title">{{ title }}</p>
        <p class="event-date">{{ date }}</p>
        <img :src="avatar" class="event-avatar" :title="name" />
        <p class="event-description">{{ description }}</p>

        <p class="show-more" @click="showPerks = !showPerks">more details <i class="fas fa-chevron-down" v-if="showPerks === false"></i> <i class="fas fa-chevron-up" v-if="showPerks === true"></i></p>

        <div class="perks" v-if="showPerks === true">

            <p class="skills-title">Skills Required</p>
            <ul class="skills-required-ul">
                <li v-for="skills in skills_required" :key="skills">{{ skills }}</li>
            </ul>

            <p class="application-title">Application Process</p>
            <ul class="application-process-ul">
                <li v-for="applications in application_process" :key="applications">{{ applications }}</li>
            </ul>

            <p class="gain-title">Skills Gain</p>
            <ul class="skills-gain-ul">
                <li v-for="skills in skills_gain" :key="skills">{{ skills }}</li>
            </ul>

        </div>

        <button class="event-apply">Apply</button>
        
    </div>
</template>

<script>
export default {
    name: "Event",
    data: function () {
        return {
            showPerks: false
        }
    },
    props: {
        title: String,
        date: String,
        description: String,
        name: String,
        avatar: String,
        skills_required: Array,
        application_process: Array,
        skills_gain: Array
    }
}
</script>

<style scoped>

.event {
    background-color: var(--homecolor1);
    padding: 10px 40px;
    border-radius: 5px;
    color: white;
}

.event-title {
    font-family: "Fira Code", monospace;
    font-size: 20px;
    margin-bottom: 0px;
}

.event-date {
    margin-top: 3px;
    font-family: "Fira Code", monospace;
}

.event-description {
    max-width: 600px;
}

.event-avatar {
    height: 50px;
    width: 50px;
    border-radius: 9px;
}

.skills-title {
    font-family: "Fira Code", monospace;
    padding-top: 20px;
    font-weight: bold;
}

.skills-required-ul > li {
    margin-top: 3px;
    margin-bottom: 3px;
}

.application-title {
    font-family: "Fira Code", monospace;
    padding-top: 20px;
    font-weight: bold;
}

.application-process-ul > li {
    margin-top: 3px;
    margin-bottom: 3px;
}

.gain-title {
    font-family: "Fira Code", monospace;
    padding-top: 20px;
    font-weight: bold;
}

.skills-gain-ul > li {
    margin-top: 3px;
    margin-bottom: 3px;
}

.show-more {
    font-family: "Fira Code", monospace;
    vertical-align: middle;
    cursor: pointer;
}

</style>