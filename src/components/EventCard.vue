<template>
  <div class="event-card" v-for="(even, index) in event.articles" :key="index">
    <span>@{{ even.author }} em {{ even.publishedAt }}</span>
    <h4>{{ even.title }}</h4>
    <p>{{ even.description }}</p>
  </div>
</template>

<script>
export default {
  name: "EventCard",
  props: {
    event: Object,
  }
};
</script>

<style scoped>
  .event-card{
    padding: 20px;
    width: 250px;
    cursor: pointer;
    border: 1px solid #39495c;
    margin-bottom: 18px;
  }
  .event-card:hover{
    transform: scale(1.01);
    box-shadow: 0 3px 12px 0 rgba(0, 0, 0, 0.2);
  }
</style>
