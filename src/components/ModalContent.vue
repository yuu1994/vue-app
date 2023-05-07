<template>
  <div class="backdrop">
    <div class="modal" :class="{success:theme=='success'}">
        <h1>{{ header }}</h1>
        <p>{{ content }} <span>{{ username }}</span></p>
    </div>
  </div>
</template>

<script>
export default {
    props : [
      'header' , 'content' ,'username' , 'theme'
    ]
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
      background-color: blueviolet;
      color: white;
    }
</style>