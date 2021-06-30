<template>
  <div class="events">
    <img alt="Vue logo" src="../assets/logo.png" />
    <EventCard v-for="event in events" :key="event.id" :event="event"/>
  </div>
</template>

<script>
// @ is an alias to /src
import EventCard from "@/components/EventCard.vue";

export default {
  name: "Home",
  components: {
    EventCard,
  },
  data() {
    return {
      events: [
        {
        id: 171,
        category: 'lotofacil',
        title: 'Joso de Junho',
        description: 'Arranjo combinado',
        location: 'Campo Grande',
        date: '29 Junho, 2021',
        time: '23:00',
        gameBet: true,
        organizer: 'Angelo'
      },
      {
        id: 172,
        category: 'megasena',
        title: 'Joso de Maio',
        description: 'Arranjo combinado 2',
        location: 'Campo Grande',
        date: '30 Junho, 2021',
        time: '23:00',
        gameBet: true,
        organizer: 'Caio'
      }
    ]
    }
  }
};
</script>

<style scoped>
 .events{
   display: flex;
   flex-direction: column;
   align-items: center;
 }
</style>