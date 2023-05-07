<template>
  <h1>Hello Vue</h1>
  <ModalContent header="Login Success" content="Welcome" username="Kiyotaka" theme="success" />
</template>

<script>
import ModalContent from "./components/ModalContent.vue";
export default {
  components: {
    ModalContent,
  },
};
</script>

<style scoped>
h1 {
  color: blue;
}
</style>
