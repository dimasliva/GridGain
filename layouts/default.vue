<template>
  <div class="container">
    <AdminHeader @toggleSidebar="toggle"/>
    <div class="content">
      <AdminNavbar v-if="$route.name !== 'index'" :openSidebar="openSidebar"/>
      <slot/>
    </div>

  </div>
</template>
<script>
  export default({
    data: ()=> ({
      openSidebar: false,
    }),
    methods: {
      toggle(toggle) {
        this.openSidebar = toggle
      }
    }
  })
</script>
<style scoped>
  body, html {
    height: 100%;
    width: 100%;
  }
  .container {
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    height: 100%;
  }
  .content {
    display: flex;
    height: 100%;
  }
</style>