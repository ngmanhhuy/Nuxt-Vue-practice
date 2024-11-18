<template>
    <div>
      <HeroSection />
      <WhatWeDo />
      <HowItWorks />
      <Benefits
        title="Key Benefits for Local Businesses"
        :benefits="businessBenefits"
      />
      <Benefits
        title="Key Benefits for Advertisers"
        :benefits="advertiserBenefits"
      />
      <WhyChooseUs />
      <CallToAction />
    </div>
  </template>
  
  <script>
  import HeroSection from "@/components/HeroSection.vue";
  import WhatWeDo from "@/components/WhatWeDo.vue";
  import HowItWorks from "@/components/HowItWorks.vue";
  import Benefits from "@/components/Benefits.vue";
  import WhyChooseUs from "@/components/WhyChooseUs.vue";
  import CallToAction from "@/components/CallToAction.vue";
  
  export default {
    components: {
      HeroSection,
      WhatWeDo,
      HowItWorks,
      Benefits,
      WhyChooseUs,
      CallToAction,
    },
    data() {
      return {
        businessBenefits: [
          { icon: "/images/passive-income-icon.png", title: "Earn Passive Income" },
          { icon: "/images/customer-experience-icon.png", title: "Enhance Customer Experience" },
          { icon: "/images/content-control-icon.png", title: "Complete Content Control" },
        ],
        advertiserBenefits: [
          { icon: "/images/affordable-icon.png", title: "Affordable Advertising" },
          { icon: "/images/target-icon.png", title: "Localized Targeting" },
          { icon: "/images/engagement-icon.png", title: "Higher Engagement" },
        ],
      };
    },
  };
  </script>
  