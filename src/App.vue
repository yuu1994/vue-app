<template>
  <h1>Hello Vue</h1>
  <ModalContent header="Login Success" content="Welcome" username="Kiyotaka" theme="success" />
  <FooterContent/>
</template>

<script>
import ModalContent from "./components/ModalContent.vue";
import FooterContent from "./components/FooterContent.vue"
export default {
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
