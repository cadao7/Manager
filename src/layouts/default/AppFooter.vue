<template>
  
  <Contribute ref="contribute" />
  <About ref="about" />
</template>

<script>
import About from "@/components/modal/About.vue";
import Contribute from "@/components/modal/Contribute.vue";
import { version } from "../../../package.json";

export default {
  name: "AppFooter",
  data: () => ({
    version,
    links: [
      {
        title: "Discord",
        url: "https://discord.gg/U66zvhV49B",
      },
      {
        title: "Postman",
        url: "https://www.postman.com/agenciadgcode/workspace/evolution-api/overview",
      },
      {
        title: "Evolution-Api",
        icon: "mdi-github",
        url: "https://github.com/EvolutionAPI/evolution-api",
      },
      {
        title: "Doc",
        icon: "mdi-book-open-page-variant",
        url: "https://doc.evolution-api.com",
      },
    ],
  }),
  methods: {
    
    about() {
      this.$refs.about.open();
    },
    contribute() {
      this.$refs.contribute.open();
    },
  },
  components: { Contribute, About },
};
</script>

<style></style>
