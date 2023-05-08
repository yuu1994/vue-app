<template>
  <div class="backdrop" @click.self="closeModalHandler">
    <div class="modal" :class="{success:theme=='success',delete:theme2=='delete'}">
        <h1>{{ header }}</h1>
        <p>{{ content }} <span>{{ username }}</span></p>
          <!-- <slot/> -->
        <h1>{{ header2 }}</h1>
        <p>{{ content2 }} <span>{{ username2 }}</span></p>
    </div>
  </div>
</template>

<script>
export default {
    props : [
      'header' , 'content' ,'username' , 'theme' ,
      'header2' , 'content2' ,'username2' , 'theme2'
    ],
    methods : {
      closeModalHandler(){
        this.$emit('close')
      }
    }
}
</script>

<style scoped> 
    .backdrop {
        width: 100%;
        height: 100%;
        background: rgba(0,0,0,0.5);
        position: fixed;
        top: 0;
    }
    .modal {
        width: 400px;
        padding: 20px;
        margin: 200px auto;
        border-radius: 20px;
        background-color: beige;
        text-align: center;
    }
    h1 {
      margin-bottom: 3rem;
    }
    .success {
      background-color: green;
      color: white;
    }
    .delete {
      background-color: red;
      color: white;
    }

    span {
      font-size: 2rem;
    }

</style>