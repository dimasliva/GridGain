<template>
  <div class="header">
    <div class="title">Cluster Management</div>
    <div class="bts">
      <button class="btn attach">attach</button>
      <button class="btn create">create</button>
    </div>
  </div>
</template>
<script>
  export default({
    data: ()=> ({
    }),
    methods: {

    }
  })
</script>
<style scoped>
  .header {
    width: 100%;
    font-size: 24px;
    font-weight: 400;
    line-height: 32px;
    color: #000000de;
    display: flex;
    align-items: center;
    justify-content: space-between;
  }
  .bts {
    display: flex;
    align-items: center;
  }
  .btn {
    box-sizing: border-box;
    position: relative;
    -webkit-user-select: none;
    -moz-user-select: none;
    user-select: none;
    cursor: pointer;
    outline: none;
    border: none;
    -webkit-tap-highlight-color: transparent;
    display: inline-block;
    white-space: nowrap;
    text-decoration: none;
    vertical-align: baseline;
    text-align: center;
    margin: 0;
    min-width: 64px;
    line-height: 36px;
    padding: 0 16px;
    border-radius: 4px;
    overflow: visible;
    font-size: 14px;
    font-weight: bold;
    text-transform: uppercase;
  }
  .btn.attach {
    box-shadow: 0 0 #0003,0 0 #00000024,0 0 #0000001f;
    border-color: #0000001f;
    color: #0c5ca3;
    background: transparent;
    border: 1px solid currentColor;
    border-top-color: currentcolor;
    border-right-color: currentcolor;
    border-bottom-color: currentcolor;
    border-left-color: currentcolor;
    padding: 0 15px;
    line-height: 34px;
  }
  .btn.create {
    margin-left: 10px;
    box-shadow: 0 3px 1px -2px #0003,0 2px 2px #00000024,0 1px 5px #0000001f;
    background-color: #0c5ca3;
    color: #fff;
  }
</style>