<template>
  <section ref="hero" class="hero">
    <div class="hero-content">
      <h1>Turn Unused TV Screens into a Revenue Stream</h1>
      <p>Connect with FaceItMarketing to earn revenue and reach targeted audiences.</p>
      <button @click="handleClick">Get Started Today</button>
    </div>
  </section>
</template>

<script>
export default {
  mounted() {
    // Use GSAP to animate the hero section
    this.$gsap.fromTo(
      this.$refs.hero,
      { opacity: 0, y: 50 },
      { opacity: 1, y: 0, duration: 1, ease: "power3.out" }
    );
  },
  methods: {
    handleClick() {
      alert("Get Started functionality coming soon!");
    },
  },
};
</script>

<style scoped>
.hero {
  background: linear-gradient(to right, #4facfe, #00f2fe);
  color: white;
  text-align: center;
  padding: 3em 1em;
}

.hero h1 {
  font-size: 2.5em;
}

.hero p {
  font-size: 1.2em;
}
</style>
