<template>
  <div class="footer-container">
    <p class="company-name">Vuelogist {{companyYear()}}</p>
    <a href="#" class="company-email">hello@vuelogist.com</a>
  </div>
</template>

<script setup>
  const companyYear = () => {
    return 90 + 9
  }
</script>

<style>
  .footer-container {
    display: flex;
    flex-direction: row;
    justify-content: space-around;
  }

  .company-email {
    text-decoration: none;
    color: black;
  }
</style>