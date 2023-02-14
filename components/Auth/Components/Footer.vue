<template>
    <div class="footer">
      <div class="reset">Reset Password</div>
      <div class="btns">
        <div class="singup btn">Sign Up</div>
        <div @click="signIn" class="signin btn">Sign In</div>
      </div>
    </div>
</template>
<script>
  export default({
    methods: {
      signIn() {
        this.$router.push('/Clusters')
      },
    }
  })
</script>
<style scoped>
    .footer {
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    .reset {
      cursor: pointer;
      color: #0d599b;
    }
    .reset:hover {
      text-decoration: underline;
    }
    .btns {
      display: flex;
      align-items: center;
    }
    .btn {
      text-transform: uppercase;
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
      font-weight: 500;
      font-family: Roboto,Helvetica Neue,sans-serif;
      font-size: 14px;
    }
    .singup {
      box-shadow: 0 0 #0003,0 0 #00000024,0 0 #0000001f;
      border-color: #0000001f;
      color: #0c5391;
      background: transparent;
      border: 1px solid currentColor;
      margin-right: 10px;
    }
    .signin {
      box-shadow: 0 3px 1px -2px #0003,0 2px 2px #00000024,0 1px 5px #0000001f;
      background-color: #0c5ca3;
      color: #fff;
    }
  </style>