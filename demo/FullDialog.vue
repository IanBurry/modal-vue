<template>
  <modal :showModal="showModal" :closeAction="closeAction" :largeModal="largeModal">
    <h1 slot="header">Full Dialog</h1>
    <span slot="body">
      Not such a <strong>fool!</strong>
      <span v-if="largeModal">Now even larger!</span>
    </span>
    <div slot="footer">
      <button @click="clickAction">Start again</button>
    </div>
  </modal>
</template>

<script>
  import Modal from 'modal-vue'
  export default {
    props: ['showModal', 'closeAction', 'clickAction', 'largeModal'],
    components: { Modal }
  }
</script>

<style scoped>

</style>