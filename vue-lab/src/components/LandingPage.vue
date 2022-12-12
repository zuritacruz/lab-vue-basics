<template>
  <div class="landing-page-container">
    <h1 class="landing-title">Are you logged in?</h1>
    <p class="landing-text" :class="bgColor" v-if="loggedIn">You are logged in, yay!</p>
    <p class="landing-text" :class="bgColor" v-else>You are not logged in, tsk!</p>
    <button v-if="!loggedIn" @click="logInOut">Log In</button>
    <button v-else @click="logInOut">Log Out</button>
  </div>
</template>

<script setup>
  import { ref } from 'vue';
  let loggedIn = ref(true);
  let bgColor = ref('green')

  const logInOut = () => {
    if (loggedIn.value) {
      loggedIn.value = false;
      bgColor.value = 'red';
    } else {
      loggedIn.value = true;
      bgColor.value = 'green';
    }
  }


</script>

<style>
  .landing-page-container {
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .green {
    background-color: rgb(133, 255, 133);
  }

  .red {
    background-color: rgb(250, 130, 130);
  }
</style>