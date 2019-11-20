<template>
  <div id="app">
    <div class="modal" v-if="showModal">
      <textarea v-model="textValue"></textarea>
      <div @click="confirm"><input type="button" value="确定"></div>
      <div @click="close()"><input type="button" value="关闭"></div>
    </div>
    <div class="box">
      <h2 class="clearfix">
        <div class="add" @click="openModal">+</div>
        &nbsp;待&nbsp;&nbsp;办&nbsp;&nbsp;事&nbsp;项
      </h2>
      <div class="content">


        <div class="list-item" v-for="(item, index) of list" :key="item-index" @click="deleteItem(index)">
          <div></div>
          {{index + 1}}. {{item}}

        </div>
      </div>
    </div>
  </div>


</template>

<script>
  export default {
    name: 'app',
    data() {
      return {
        showModal: false,
        list: [
          '123',
          '1234',
          '1235',
          '1236',
        ],
        textValue: ''
      }
    },
    methods: {
      openModal() {
        // eslint-disable-next-line no-console
        console.log(1)
        this.showModal = true
      },
      close() {
        this.showModal = false
      },
      confirm() {
        this.list.push(this.textValue)
        this.textValue = ''
        this.showModal = false
      },
      deleteItem(index) {
        this.list.splice(index, 1)
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
    border: 2px solid;
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
    color: orange;
  }


  .content {
    width: 400px;
    height: 40px;
    margin: 20px auto;
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
    height: 240px;
    z-index: 15;
    background: whitesmoke;
    border: 2px solid orange;
  }




</style>
