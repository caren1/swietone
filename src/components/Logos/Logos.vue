<template>
  <section>
    <div class="logos" v-if="logos">
      <SingleLogo
        :logo="logo"
        v-for="logo in logos"
        :key="logo.alt"
      />
    </div>
  </section>
</template>

<script>
import SingleLogo from './SingleLogo.vue'
export default {
  components: { SingleLogo },
  data() {
    return {
      logos: [
        {
          alt: "elsafe-logo",
          path: require("@/assets/svg/logos/elsafe.svg"),
        },
        {
          alt: "w2-logo",
          path: require("@/assets/svg/logos/w2.svg"),
        },
        {
          alt: "moon-logo",
          path: require("@/assets/svg/logos/moon.svg"),
        },
        {
          alt: "zsips-logo",
          path: require("@/assets/svg/logos/zsips.svg"),
        },
        {
          alt: "theflier-logo",
          path: require("@/assets/svg/logos/theflier.svg"),
        },
        {
          alt: "torch-logo",
          path: require("@/assets/svg/logos/torch.svg"),
        },
        {
          alt: "w1-logo",
          path: require("@/assets/svg/logos/w1.svg"),
        },
        {
          alt: "mctrade-logo",
          path: require("@/assets/svg/logos/mct.svg"),
        },
        {
          alt: "swietone-logo",
          path: require("@/assets/svg/logos/swietone.svg"),
        },
        {
          alt: "gswet-logo",
          path: require("@/assets/svg/logos/gswet.svg"),
        },
        {
          alt: "w3-logo",
          path: require("@/assets/svg/logos/w3.svg"),
        },
        {
          alt: "trener-logo",
          path: require("@/assets/svg/logos/trener.svg"),
        },
        {
          alt: "gswet.store-logo",
          path: require("@/assets/svg/logos/gswetstore.svg"),
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
@import "@/assets/_variables.scss";

section {
  display: flex;
  align-items: center;
  min-height: 100vh;
  height: 100%;
  width: 100vw;
  position: relative;

  .logos {
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    justify-content: space-evenly;
    max-width: 80%;
    margin: auto;
    // max-height: 80%;
    // border: 1px solid $white;
  }
}
</style>
