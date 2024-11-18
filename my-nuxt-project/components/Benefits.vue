<template>
    <section class="benefits">
      <h2>{{ title }}</h2>
      <div class="cards">
        <div class="card" v-for="(benefit, index) in benefits" :key="index">
          <img :src="benefit.icon" :alt="benefit.title" />
          <h3>{{ benefit.title }}</h3>
        </div>
      </div>
    </section>
  </template>
  
  <script>
  export default {
    props: {
      title: String,
      benefits: Array,
    },
  };
  </script>
  
  <style scoped>
  .cards {
    display: flex;
    justify-content: space-around;
  }
  
  .card {
    text-align: center;
    max-width: 30%;
  }
  
  .card img {
    max-width: 80px;
    margin-bottom: 1em;
  }
  </style>
  