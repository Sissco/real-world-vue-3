<template>
  <div class="events">
    <h1>Event For Good</h1>
    <!-- <img alt="Vue logo" src="../assets/logo.png" /> -->

    <!-- :event="event" means that we're adding an event prop and passing the event object that we're currently iterating over-->
    <EventCard v-for="event in events" :key="event.id" :event="event" />
  </div>
</template>

<script>
// @ is an alias to /src
import EventCard from "@/components/EventCard.vue";
import EventService from "@/services/EventService.js";

export default {
  name: "EventList",
  components: {
    EventCard,
  },
  data() {
    return {
      events: null,
    };
  },
  created() {
    EventService.getEvents()
      .then((response) => {
        this.events = response.data;
      })
      .catch((error) => console.log(error));
  },
};
</script>

<style scoped>
.events {
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>
