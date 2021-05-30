<template>
<h1>hi there</h1>
  <div class="events">
    <EventCard v-for="event in events" :key="event.id" :event="event" />
  </div>
</template>

<script>
// @ is an alias to /src
import EventCard from "@/components/EventCard.vue";

export default {
  name: "Home",
  components: {
    EventCard
  },
  data() {
    return{
    events: [
      {
        id: 5928101,
        category: "animals",
        title: "adoption day",
        description: "cat cat dog",
        location: "house",
        date: "tuesday",
        time: "noon",
        petsAllowed: true,
        organizer: "me"
      },
      {
        id: 5928191,
        category: "houses",
        title: "donate a house item",
        description: "yep",
        location: "house",
        date: "thursday",
        time: "noonthirty",
        petsAllowed: false,
        organizer: "me"
      },
      {
        id: 5988101,
        category: "animals",
        title: "snack day",
        description: "cat dog cat",
        location: "yard",
        date: "friday",
        time: "evening",
        petsAllowed: true,
        organizer: "fred"
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
