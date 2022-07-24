<template>
  <h1>Events for good</h1>
  <div class="events">
    <EventCard v-for="event in events" :key="event.id" :event="event" />
  </div>
</template>

<script>
// @ is an alias to /src
import EventCard from '@/components/EventCard.vue'

export default {
  name: 'Home',
  components: {
    EventCard
  },
  data() {
    return {
      events: [
        {
          id: 1322423232,
          category: 'Animal welfare',
          title: 'Cat Adoption Day',
          description: 'Find your new feline friends at this event.',
          location: 'Meow Town',
          date: 'January 26, 2023',
          time: '12:00',
          petsAllowed: true,
          organizer: 'Cat Laydee'
        },
        {
          id: 13224232,
          category: 'Animal welfare',
          title: 'Cat Adoption Day Feb',
          description: 'Find your new feline friends at this event.',
          location: 'Meow Town',
          date: 'February 26, 2023',
          time: '10:00',
          petsAllowed: true,
          organizer: 'Cat Laydee'
        }
      ]
    }
  }
}
</script>
<style scoped>
.events {
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>
