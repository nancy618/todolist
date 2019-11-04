<template>
  <div id="app">
    <div class="box">
      <h2>&nbsp;待&nbsp;办&nbsp;事&nbsp;项</h2>
      <div class="content">
        <input class="input1" type="text" >
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'app',
  components: {
  }
}
</script>

<style>
  .box {
    width: 600px;
    height: 400px;
    border: 2px solid gray ;
    padding: 10px 5px 8px 15px;
    position: absolute;
    top: 50%;
    left: 45%;
    margin-left: -250px;
    margin-top: -200px;

  }
  h2{
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

  .btn1 {
    float: right;
  }

  .content li {
    line-height: 40px;
  }
</style>
