<template>
  <h1>Hello Vue</h1>
  <div class="" v-if="showModal">
    <ModalContent :header="header" :content="content" :username="username" :theme="theme" @close="showModal=false">
      <h1>{{ header }}</h1>
      <p>{{ content }} <span>{{ username }}</span></p>
    </ModalContent>
  </div>
  <button @click="showModal=!showModal">
    <span v-if="!showModal">Show Modal</span>
    <span v-if="showModal">hide Modal</span>
  </button>
  <br>
  <br>

  <div class="" v-if="showModal2">
    <ModalContent :header2="header2" :content2="content2" :username2="username2" :theme2="theme2" @close="showModal2=false"/>
  </div>


  <button @click="showModal2=!showModal2">Click</button>
  
  <FooterContent/>
</template>

<script>
import ModalContent from "./components/ModalContent.vue";
import FooterContent from "./components/FooterContent.vue"
export default {
    data(){
      return {
        header : "Login success",
        content : "Welcome ",
        username : "kei",
        theme : "success",
        showModal : false ,

        header2 : "Delete Success",
        content2 : "We are really sorry for inconvnience ",
        username2 : "Yuu",
        theme2 : "delete",
        showModal2 : false ,

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
