<template>
    <section class="why-choose-us">
      <h2>Why Choose FaceItMarketing?</h2>
      <ul>
        <li v-for="(feature, index) in features" :key="index">{{ feature }}</li>
      </ul>
      <blockquote>
        "FaceItMarketing has transformed how we connect with our community while generating extra revenue!"
      </blockquote>
    </section>
  </template>
  
  <script>
  export default {
    data() {
      return {
        features: ["Ease of Use", "Powerful Analytics Tools", "Trusted Network of Local Partners"],
      };
    },
  };
  </script>
  
  <style scoped>
  blockquote {
    font-style: italic;
    margin-top: 1em;
    color: #555;
  }
  </style>
  