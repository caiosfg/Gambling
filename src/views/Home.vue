<template>
  <div class="events">
    <img alt="Vue logo" src="../assets/logo.png" />
    <EventCard v-for="event in events" :key="event.id" :event="event"/>
  </div>
</template>

<script>
import EventCard from "@/components/EventCard.vue";
import axios from "axios";

export default {
  name: "Home",
  components: {
    EventCard,
  },
  data() {
    return {
      events: null,
    };
  },
  created() {
    axios
      .get(
        "https://newsapi.org/v2/everything?q=Apple&from=2021-07-12&sortBy=popularity&apiKey=ceaba1de004448138d8411e70a681980"
      )
      .then((response) => (this.events = response))
      .catch(error => {
        console.log(error)
      })
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
