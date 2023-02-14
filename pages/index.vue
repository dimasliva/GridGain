<template>
  <div class="container">
    <AuthHeader/>
    <div class="modal_signin">
      <AuthSignIn/>
    </div>
  </div>
</template>
<script>
export default {
    layout: "default",
}
</script>
<style scoped>
.container {
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
.modal_signin {
  width: 648px;
  margin-top: 30px;
}
</style>