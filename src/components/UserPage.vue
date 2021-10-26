<template>
  <div class="user-page pt-5">
    <button type="button" class="btn btn-primary" 
      @click="openModal">
      OpenModal
    </button>
    <Modal
      v-if="isModalOpen"
      title="Очень важнач информация"
      @close="isModalOpen = false"
    />
  </div>
</template>

<script>

import Modal from './Modal'

export default {
  name: 'UserPage',
  components: {
    Modal
  },
  data(){
    return{
      isModalOpen :false
    }
  },
  methods: {
    openModal(){
      this.isModalOpen = true
    }
  }
  
}
</script>


