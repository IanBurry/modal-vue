<template>
  <modal :showModal="showModal" :closeAction="closeAction">
    <h1 slot="header">Simple Dialog</h1>
    <form slot="body" @submit.prevent="OnSubmit">
      <div>
        <label for="name"></label>
        <input type="text" name="name">
      </div>
      <div>
        <button type="submit">Save</button>
        <button type="submit">Blah</button>
        <button type="button">Delete</button>
      </div>
    </form>
  </modal>
</template>

<script>
  import Modal from 'modal-vue'
  export default {
    props: ['showModal', 'closeAction'],
    components: { Modal },
    methods: {
      OnSubmit() {
        console.log('Submitting...')
      }
    }
  }
</script>

<style scoped>

</style>