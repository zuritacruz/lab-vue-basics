<template>
  <Navbar />
  <LandingPage />
  <section class="cards-section">
    <div class="cards-container" v-for="pokemon in pokemonList">
      <img :src='pokemon.img' alt="Pokemon image" class="card-img">
      <h1 class="card-title">{{ pokemon.title }}</h1>
      <p class="card-description">{{ pokemon.description }}</p>
      <div class="card-content-container">
        <h2 class="card-content-title">Main move:</h2>
        <p class="card-content">{{ pokemon.content }}</p>
      </div>
    </div>
  </section>
  <Footer />
</template>

<script setup>
  import { ref } from 'vue';
  import Navbar from './components/Navbar.vue';
  import LandingPage from './components/LandingPage.vue';
  import Footer from './components/Footer.vue';

const pokemonList = ref([
  {
    img: 'https://freepngimg.com/save/37470-pikachu-transparent-background/1254x1254',
    title: 'Pikachu',
    description: 'Small electric mouse',
    content: 'Thunderbolt'
  },
  {
    title: 'Charmander',
    img: 'https://www.pngmart.com/files/22/Charmander-Pokemon-Transparent-Background.png',
    description: 'Small fire salamander',
    content: 'Ember'
  },
  {
    title: 'Squirtle',
    img: 'https://assets.stickpng.com/images/580b57fcd9996e24bc43c32a.png',
    description: 'Small water turtle',
    content: 'Water gun'
  },
  {
    title: 'Bulbasaur',
    img: 'https://www.pngmart.com/files/11/Pokemon-Bulbasaur-PNG-File.png',
    description: 'Small leafy toad',
    content: 'Vine whip'
  },
  {
    title: 'Mewtwo',
    img: 'https://freepngimg.com/save/120880-pic-mewtwo-free-transparent-image-hq/1045x1280',
    description: 'Lab created humanoid creature',
    content: 'Psystrike'
  },
  {
    title: 'Mew',
    img: 'https://www.pngmart.com/files/22/Mew-Pokemon-PNG-Isolated-HD-Pictures.png',
    description: 'Celestial alien like creature',
    content: 'Psychic'
  }
]);

</script>

<style scoped>
  .cards-section {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-gap: 15px;
    margin: 50px;
    justify-items: center;
    padding: 10px;
  }

  .card-container {
    max-width: 200px;
  }

  .card-img {
    width: 200px;
    max-width: 200px;
    height: 300px;
    object-fit: contain;
  }

  .card-title {
    text-align: center;
    margin: 0;
  }

  .card-description {
    text-align: center;
    font-size: 14px;
  }

  .card-content-container {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
  }

  .card-content-title, .card-content {
    font-size: 16px;
  }

</style>
