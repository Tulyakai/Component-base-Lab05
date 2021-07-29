<template>
  <p>Edit the event here</p>
  <button @click="edit">Edit Me</button>
</template>

<script>
export default {
  props: ['event'],
  inject: ['Gstore'],
  methods: {
    edit() {
      this.Gstore.flashMessageEdit = this.event.title + ' has been updated'
      setTimeout(() => {
        this.Gstore.flashMessageEdit = ''
      }, 3000)
      this.$router.push({ name: 'EventDetails' })
    }
  }
}
</script>
