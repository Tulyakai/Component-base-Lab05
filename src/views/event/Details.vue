<template>
  <p>{{ event.time }} on {{ event.date }} @ {{ event.location }}</p>
  <p>{{ event.description }}</p>
  <div id="flashMessage" v-if="Gstore.flashMessageEdit">
    {{ Gstore.flashMessageEdit }}
  </div>
</template>

<script>
export default {
  props: ['event'],
  inject: ['Gstore']
}
</script>

<style scoped>
@keyframes yellowfade {
  from {
    background: lightgreen;
  }
  to {
    background: transparent;
  }
}

#flashMessage {
  animation-name: yellowfade;
  animation-duration: 3s;
}
</style>
