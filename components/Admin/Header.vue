<template>
  <div class="header">
      <div class="start">
      <span class="toggle" @click="toggle">
        <v-icon large color="white darken-2 "> mdi-tally-mark-3</v-icon>
      </span>
      <span class="logo">
        <img src="~/assets/icons/header/logo.png"/>
      </span>
    </div>
    <div class="end">
      <span class="about">
        <span class="support">Support</span>
        <span class="icon slack">
          <img src="~/assets/icons/header/slack.svg"/>
        </span>
        <span class="icon discord">
          <img src="~/assets/icons/header/discord.svg"/>
        </span>
      </span>
      <span class="activity">
        <span class="icon success">
          <v-icon large color="white darken-2 "> mdi-check-circle</v-icon>
        </span>
        <span class="nickname">hardcore_chaplygin</span>
      </span>
      <span class="icon alert">
        <v-icon large color="white darken-2 "> mdi-bell</v-icon>
      </span>
      <span class="user">
        <v-icon large color="white darken-2 "> mdi-account-circle</v-icon>
      </span>
    </div>
  </div>
</template>
<script>
  export default({
    data: ()=> ({
      openSidebar: false,
    }),
    methods: {
      toggle() {
        this.openSidebar = !this.openSidebar
        this.$emit('toggleSidebar', this.openSidebar)
      }
    }
  })
</script>
<style scoped>
  .header {
    background-color: #0058bb;
    width: 100%;
    height: 64px;
    color: white;
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 0px 30px;
    padding-right: 0px;
  }
  .toggle {
    cursor: pointer;
    transform: rotate(90deg) scale(1.2);
  }
  .start, .end {
    display: flex;
    align-items: center;
    height: 100%;
  }
  .logo {
    margin-left: 50px;
    margin-bottom: 5px;
    height: 100%;
  }
  .logo img {
    height: 100%;
    filter: invert(1) brightness(100) sepia(97%);
  }
  .about {
    height: 100%;
    display: flex;
    align-items: center;
  }
  .user, .alert, .activity {
    height: 100%;
    display: flex;
    align-items: center;
    border-left: 1px solid #003c88;
    padding: 0 25px;
  }
  .alert {
    display: flex;
    align-items: center;
  }
  .user, .user i, .icon, .icon img {
    height: 100%;
  }
  .user i {
    font-size: 38px;
  }
  .slack, .discord, .support {
    height: 40%;
    padding: 0 10px;
  }
  .discord {
    margin-right: 20px;
  }
  .support {
    text-decoration: underline;
    font-size: 16px;
    font-weight: bold;
  }
  .success {
    filter: invert(40%) sepia(83%) saturate(4317%) hue-rotate(112deg) brightness(104%) contrast(99%);
    margin-right: 10px;
    display: flex;
    align-items: center;
  }
  .nickname {
    font-weight: bold;
  }
</style>