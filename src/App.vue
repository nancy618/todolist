<template>
  <div id="app">
    <div class="modal" v-if="showModal">

    </div>
    <div class="box">
      <h2 @click="openModal" class="clearfix">
        <div class="add">+</div>
        &nbsp;待&nbsp;&nbsp;办&nbsp;&nbsp;事&nbsp;项
      </h2>
      <div class="content">


        <div class="input1">臭木木猪🐖</div>


      </div>
    </div>
  </div>


</template>

<script>
  export default {
    name: 'app',
    data() {
      return {
        showModal: false
      }
    },
    methods: {
      openModal() {
        // eslint-disable-next-line no-console
        console.log(1)
        this.showModal = true
      }
    }
  }
</script>

<style>
  .clearfix::after {
    content: '';
    display: table;
    clear: both;
  }

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

  .add {
    border: 2px solid ;
    border-radius: 25px;
    width: 30px;
    height: 30px;
    color: #ccc;
    transition: color .25s;
    float: left;
    line-height: 30px;
    text-align: center;
  }


  .add:hover {
    color: pink;
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
    width: 400px;
    height: 260px;
    z-index: 15;
    background: pink;
  }


</style>
