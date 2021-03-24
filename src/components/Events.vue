<template>
    <div class="events">
        <Event :title="event.event_title" :date="event.event_date" :description="event.event_description" :name="event.event_owner.name" :avatar="event.event_owner.avatar" :skills_required="event.skills_required" :application_process="event.application_process" :skills_gain="event.skills_gain" />
    </div>
</template>

<script>
import Event from "./Event.vue";

export default {
    name: "Events",
    data: function() {
        return {
            event: {
                event_title: "Pytorch | Machine Learning",
                event_date: "02/02/2021",
                event_description: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.",
                event_owner: {
                    name: "Khaleel Gibran",
                    avatar: "https://cdn.khaleelgibran.com/donut.png"
                },
                skills_required: ["Git", "Marvel Knowledge", "Python"],
                application_process: ["Application Review", "Demo Test", "Review"],
                skills_gain: ["Marvel Comic Knowledge", "DC Knowledge"]
            }
        }
    },
    components: {
        Event
    },
}
</script>

<style scoped>

</style>