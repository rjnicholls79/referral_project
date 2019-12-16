<template>
<div id="app" class="">
  <!--<div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>
    <router-view/>-->
    <transition name="fade">
    <section class="log-in" v-if="isShow['Log']">
      <h2>please sign in</h2>
      <input type="input" placeholder="User Name">
      <input type="password" placeholder="Password">
      <p>Lost Your Credentials</p>
    </section>
  </transition>
  <section class="signIn" v-if="isShow['Sign']">
    <h2 class="text-center">please sign in</h2>
    <div class="mx-auto d-block sign-arrow" @click="isShow['Log'] = !isShow['Log']; isShow['Sign'] = !isShow['Sign']"><i class="fas fa-chevron-down"></i></div>
  </section>
  <section class="container">
    <section class="main-illustration">
      <img alt="House" src="./assets/Img_Asset.svg" class="mx-auto d-block">
    </section><!-- End Main Illustration -->
    <section class="logo">
      <img alt="House" src="./assets/Logo_Asset.svg" class="mx-auto d-block">
    </section><!-- End logo -->
    <h1 class="text-center mt-2">welcome to our online referral portal</h1>
  </section><!-- End Container -->
</div>
</template>

<script>
// @ is an alias to /src

export default {
  name: 'home',
  components: {
  },
  data(){
    return{
      isShow:{
        'Sign': true,
        'Log': false,
      }
    }
  },


}
</script>

<style lang="scss">
@import "./styles/universal.scss";
@import "./styles/log-in.scss";
</style>
