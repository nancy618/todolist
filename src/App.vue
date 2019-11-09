<template>
  <div id="app">
    <div class="modal" v-if="showModal">

    </div>
    <div class="box">
      <h2 @click="openModal">&nbsp;待&nbsp;办&nbsp;事&nbsp;项</h2>
      <div class="content">

        <input class="input1" type="text" v-model="value">


      </div>
    </div>
  </div>


</template>

<script>
  export default {
    name: 'app',
    data () {
      return {
        showModal: false
      }
    },
    methods: {
      openModal () {
        this.showModal = false
      }
    }
  }
</script>

<style>
  .box {
    width: 600px;
    height: 400px;
    border: 2px solid gray;
    padding: 10px 5px 8px 15px;
    position: absolute;
    top: 50%;
    left: 45%;
    margin-left: -250px;
    margin-top: -200px;

  }

  h2 {
    text-align: center;
  }

  .content {
    width: 400px;
    height: 40px;
    margin: 20px auto;
  }

  .input1 {
    margin-bottom: 20px;
    width: 400px;
    height: 40px;

  }

  .content li {
    line-height: 40px;
  }

  .modal {
    position: fixed;
    left: 0;
    right: 0;
    top: 0;
    bottom: 0;
    margin: auto;
    width: 200px;
    height: 260px;
    z-index: 15;
    background: pink;
  }

</style>
