<template>
  <h1>Hello Vue</h1>
  <div class="" v-if="showModal">
    <ModalContent :header="header" :content="content" :username="username" :theme="theme" @close="showModal=false" />
  </div>
  <button @click="showModal=!showModal">
    <span v-if="!showModal">Show Modal</span>
    <span v-if="showModal">hide Modal</span>
  </button>
  <FooterContent/>
</template>

<script>
import ModalContent from "./components/ModalContent.vue";
import FooterContent from "./components/FooterContent.vue"
export default {
    data(){
      return {
        header : "Delete success",
        content : "we are very sorry for inconvenience",
        username : "kei",
        theme : "delete",
        showModal : false ,
      }
    },
  components: {
    ModalContent , FooterContent 
  },
};
</script>

<style scoped>
h1 {
  color: blue;
}
</style>
