<template>
  <div class="signwith">
    <div class="title">Sign in to your account with</div>

    <div class="btns">
      <div class="google">

        <div id="gSignInWrapper" @click="signIn">
          <div  class="customGPlusSignIn">
            <img src="@/assets/icons/auth/google.svg"/>
          </div>
        </div>

      </div>
      <div class="microsoft">
        <div class="customGPlusSignIn">
            <img src="@/assets/icons/auth/microsoft.svg"/>
        </div>
      </div>
    </div>

    <div class="or">
      <div class="line"></div>
      <span>or</span>
      <div class="line"></div>
    </div>

    <div class="inputs">

      <div class="input_container">
        <label for="email">Email</label>
        <div class="input">
          <input id="email"/>
        </div>
        <span></span>
      </div>
    
      <div class="input_container">
        <label for="email">Password</label>
        <div class="input">
          <input id="email" type="password"/>
        </div>
        <span></span>
      </div>

    </div>
  </div>
</template>
<script>
  export default({
    name: "SignWith",
    data: () => ({
    }), 
    methods: {
      signIn() {
        this.$router.push('/Clusters')
      }

    },
    mounted() {

    },
  })
</script>
<style scoped>
  .signwith {
    display: flex;
    flex-direction: column;
    align-items: center;
  }
  .title {
    color:#000000de;
    font-family: Roboto,Helvetica Neue,sans-serif;
  }
  .btns {
    display: flex;
    align-items: center;
    margin: 20px 0px;
  }
  .customGPlusSignIn {
    display: flex;
    align-items: center;
    justify-content: center;
    background: white;
    color: #444;
    width: 50px;
    height: 50px;
    border-radius: 55%;
    border: 1px solid rgb(172, 172, 172);
    white-space: nowrap;
    cursor: pointer;
  }
    #customGPlusSignIn:hover {
      cursor: pointer;
    }
    span.label {
      font-family: serif;
      font-weight: normal;
    }
    .customGPlusSignIn img {
      height: 50%;
      margin: auto;
    }
    span.buttonText {
      display: inline-block;
      vertical-align: middle;
      padding-left: 42px;
      padding-right: 42px;
      font-size: 14px;
      font-weight: bold;
      /* Use the Roboto font that is loaded in the <head> */
      font-family: 'Roboto', sans-serif;
    }
  .microsoft {
    margin-left: 20px;
  }
  .or {
    display: flex;
    align-items: center;
  }
  .or span {
    margin: 0 5px;
  }
  .line {
    width: 60px;
    border: 1px solid transparent;
    border-top-color: #0000001f;
  }
  .inputs {
    display: flex;
    align-items: flex-start;
    justify-content: space-between;
    width: 100%;
    margin: 30px;
  }
  .input_container {
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    width: 49%;
  }
  .input_container label {
    font-size: 12px;
    font-weight: 400;
    font-family: Roboto,Helvetica Neue,sans-serif;
  }
  .input {
    width: 100%;
    border-bottom: 1px solid gray;
  }
  input {
    width: 100%;
    outline: none;
    padding: 4px 0px;
  }
</style>