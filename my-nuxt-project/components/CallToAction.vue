<template>
  <section ref="cta" class="cta">
    <h2>Take the Next Step!</h2>
    <div class="cta-buttons">
      <button @click="businessClick">Turn TVs into Revenue!</button>
      <button @click="advertiserClick">Reach Local Audiences!</button>
    </div>
  </section>
</template>

<script>
export default {
  mounted() {
    // Bounce animation for the buttons
    this.$gsap.fromTo(
      this.$refs.cta.querySelectorAll("button"),
      { scale: 0.9 },
      {
        scale: 1,
        duration: 0.5,
        ease: "bounce.out",
        repeat: -1,
        yoyo: true,
        stagger: 0.2,
      }
    );
  },
  methods: {
    businessClick() {
      alert("Sign-up functionality for businesses coming soon!");
    },
    advertiserClick() {
      alert("Sign-up functionality for advertisers coming soon!");
    },
  },
};
</script>

<style scoped>
.cta {
  text-align: center;
  background: #4facfe;
  color: white;
  padding: 2em 1em;
}

.cta-buttons button {
  margin: 0.5em;
}
</style>
