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
  <UDashboardPanel id="fullCalendar">
    <template #header>
      <UDashboardNavbar title="FullCalendar">
        <template #leading>
          <UDashboardSidebarCollapse />
        </template>
        <template #right>
          <ULink to="https://fullcalendar.io/" target="_blank">Full Calendar Documentation</ULink>
        </template>
      </UDashboardNavbar>
    </template>

    <template #body>
      <UContainer>
        <FullCalendar :options="calendarOptions" />
      </UContainer>
    </template>
  </UDashboardPanel>
</template>
