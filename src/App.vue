<template>
  <h1>Hello Vue</h1>
  <ModalContent :header="header" :content="content" :username="username" :theme="theme" />
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
        theme : "delete"
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
