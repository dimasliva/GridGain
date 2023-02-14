<template>
  <div class="modal">
    <div class="header_signin">Sign In</div>
    <div class="content">
      <AuthComponentsSignWith/>
      <AuthComponentsFooter/>
    </div>
  </div>
</template>
<style scoped>
.modal {
  width: 100%;
}
.header_signin {
    border-top-left-radius: 4px;
    border-top-right-radius: 4px;
    padding-top: 2px;
    height: 74px;
    background-color: #0d5ea6;
    color: #fff;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 34px;
    font-weight: 400;
    line-height: 45px;
  }
  .content {
    padding: 24px;
    box-shadow: 0 2px 1px -1px #0003,0 1px 1px #00000024,0 1px 3px #0000001f;
  }
</style>