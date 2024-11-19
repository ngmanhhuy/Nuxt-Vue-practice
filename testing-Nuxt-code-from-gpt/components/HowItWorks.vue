<template>
  <section ref="howItWorks" class="how-it-works">
    <h2>How It Works</h2>
    <div ref="steps" class="steps">
      <div class="step" v-for="(step, index) in steps" :key="index">
        <img :src="step.icon" :alt="step.title" />
        <p><strong>{{ step.title }}</strong></p>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      steps: [
        { icon: "/images/install-icon.png", title: "Step 1: Installation Made Easy" },
        { icon: "/images/web-app-icon.png", title: "Step 2: Ad Management via Web App" },
        { icon: "/images/revenue-icon.png", title: "Step 3: Revenue Generation" },
      ],
    };
  },
  mounted() {
    // Stagger animations for steps
    this.$gsap.fromTo(
      this.$refs.steps.children,
      { opacity: 0, y: 50 },
      {
        opacity: 1,
        y: 0,
        duration: 1,
        stagger: 0.3,
        ease: "power3.out",
      }
    );
  },
};
</script>

<style scoped>
.steps {
  display: flex;
  justify-content: center;
  gap: 2em;
}

.step img {
  max-width: 60px;
}

.step p {
  text-align: center;
  font-size: 1.1em;
}
</style>
