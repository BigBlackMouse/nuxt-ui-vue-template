<script setup lang="ts">
import FullCalendar from '@fullcalendar/vue3'
import dayGridPlugin from '@fullcalendar/daygrid'
import interactionPlugin from '@fullcalendar/interaction'

const calendarOptions = {
  plugins: [ dayGridPlugin, interactionPlugin ],
  initialView: 'dayGridMonth'
}
</script>
<template>
  <UContainer>
    <FullCalendar :options="calendarOptions" />
  </UContainer>
</template>
