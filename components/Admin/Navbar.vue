<template>
  <div class="navbar" :class="{'active': openSidebar}">
      <div class="blocks">
      <div class="block" :class="{'active': $route.path === '/'}">
        <span class="icon mdi mdi-file-tree"></span>
        <span class="link">
          <NuxtLink to="/">Clusters</NuxtLink>
        </span>
      </div>

      <div class="block">
        <span class="icon mdi mdi-view-dashboard"></span>
        <span class="link">
          <NuxtLink to="/">Dashboard</NuxtLink>
        </span>
      </div>

      <div class="block">
        <span class="icon mdi mdi-bell"></span>
        <span class="link">
          <NuxtLink to="/">Alterting</NuxtLink>
        </span>
      </div>

      <div class="block">
        <div class="icon tracing">
          <img src="~/assets/icons/navbar/tracing.svg"/>
        </div>
        <span class="link">
          <NuxtLink to="/">Tracing</NuxtLink>
        </span>
      </div>

      <div class="block">
        <span class="icon sql mdi mdi-database-search"></span>
        <span class="link">
          <NuxtLink to="/">SQL</NuxtLink>
        </span>
      </div>

      <div class="block">
        <span class="icon mdi mdi-file-code"></span>
        <span class="link">
          <NuxtLink to="/">Compute</NuxtLink>
        </span>
      </div>

      <div class="block">
        <div class="icon deployment">
          <img src="~/assets/icons/navbar/deployment.svg"/>
        </div>
        <span class="link">
          <NuxtLink to="/">Deployment</NuxtLink>
        </span>
      </div>

      <div class="block">
        <span class="icon mdi mdi-server"></span>
        <span class="link">
          <NuxtLink to="/">Caches</NuxtLink>
        </span>
      </div>
    </div>

    <span v-if="!openSidebar" class="icon logo">
      <img src="~/assets/icons/navbar/navIcon.svg"/>
    </span>
    <div v-else class="footer_container">
      <div class="privacy">
        <div class="text">GridGain Nebula</div>
        <div class="text">www.gridgain.com</div>
        <div class="text">Terms and Conditions</div>
        <div class="text">Copyright © 2023 GridGain Systems, Inc. All Rights Reserved.</div>
        <div class="text">Apache, Apache Ignite, the Apache feather and the Apache Ignite logo are trademarks of The Apache Software Foundation.</div>
      </div>
      <div class="footer">
        <img src="~/assets/icons/navbar/navIcon.svg"/>
        <a class="view_error">View Error Log</a>
      </div>
    </div>
  </div>
</template>
<script>
  export default({
    data: ()=> ({
    }),
    props: {
      openSidebar: Boolean
    },
    methods: {
      toggle(toggle) {
        console.log(toggle)
      }
    },
  })
</script>
<style scoped>
  .navbar {
    background-color: #FFF;
    width: 79px;
    height: 100%;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    color: white;
    border-right: solid 1px rgba(0,0,0,.12);
    padding: 5px 0px;
    padding-bottom: 30px;
    justify-content: space-between;
  }
  .navbar.active {
    width: 259px;
  }
  .blocks {
    width: 100%;
    display: flex;
    flex-direction: column;
  }
  .block {
    display: flex;
    flex-direction: column;
    align-items: center;
    font-size: 12px;
    height: 60px;
    opacity: .7;
    cursor: pointer;
    width: 100%;
  }
  .active .block {
    align-items: center;
    flex-direction: row;
    padding-left: 20px;
  }
  .block.active .icon {
    color: #001dc0;
  }
  .block:hover {
    background-color: rgba(0,0,0,.07);
  }
  .active .block .link {
    display: flex;
    align-items: center;
    height: 45px;
    font-weight: bold;
    font-size: 16px;
  }
  .block a {
    color: #000000de;
    text-decoration: none;
  }
  .footer_container {
    display: flex;
    flex-direction: column;
    width: 100%;
    padding: 0 20px;
  }
  .privacy {
    display: flex;
    flex-direction: column;
    font-size: 12px;
    color: #000000de;
  }
  .privacy .text {
    margin: 8px 0px;
  }
  .footer {
    width: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  .footer img {
    height: 64px;
  }
  .view_error {
    color: #0b5da6;
  }
  .view_error:hover {
    text-decoration: underline
  }
  .icon {
    width: 100%;
    height: 34px;
    color: #000000de;
    font-size: 26px;
    text-align: center;
  }
  .active .block .icon {
    width: 24px;
    height: 45px;
    font-size: 30px;
    margin-right: 20px;
  }
  .active .icon img {
    height: 100%;
  }
  .active .icon.deployment {
  }
  .icon img {
    margin: auto;
    max-height: 24px;
  }
  .icon.tracing img {
    height: 20px;
  }
  .icon.deployment img {
    height: 20px;
  }
  .icon.logo {
    transform: scale(1.5);
    width: 100%;
  }
</style>