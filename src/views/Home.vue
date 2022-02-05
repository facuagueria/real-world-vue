<template>
  <div class="events">
    <h1>Events for Good</h1>
    <EventCard v-for="event in events" :key="event.id" :event="event" />
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
          id: 11111,
          category: "animal welfare",
          title: "Cat Adoption Day",
          description: "Find your new feline friend at this event.",
          location: "Meow Town",
          date: "January 28, 2022",
          time: "12:00",
          petsAllowed: true,
          organizer: "Kat Laydee",
        },
        {
          id: 22222,
          category: "animal welfare2",
          title: "Cat Adoption Day2",
          description: "Find your new feline friend at this event2.",
          location: "Meow Town2",
          date: "January 28, 20222",
          time: "12:002",
          petsAllowed: true,
          organizer: "Kat Laydee2",
        },
        {
          id: 33333,
          category: "animal welfare3",
          title: "Cat Adoption Day3",
          description: "Find your new feline friend at this event.3",
          location: "Meow Town3",
          date: "January 28, 20223",
          time: "12:003",
          petsAllowed: true,
          organizer: "Kat Laydee3",
        },
      ],
    };
  },
};
</script>
<style>
.events {
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>
