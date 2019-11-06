<template>
  <main class="schedule">
    <h1 class="page-title">Schedule</h1>
    <p class="lead">Check out this awesome schedule.</p>
    <Tickets />
    <div>
      Wait.. nothing's happening yet.
    </div>
  </main>
</template>

<script>
import Tickets from '@/components/Tickets.vue'

export default {
  components: {
    Tickets
  }
}
</script>

<style lang="scss" scoped>
@import '@/css/variables.scss';
</style>
