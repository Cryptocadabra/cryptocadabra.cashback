<template>
  <cryptocadabra-header />
  <cryptocadabra-hero />
  <cryptocadabra-process />
  <cryptocadabra-instruction />
  <cryptocadabra-rates />
  <cryptocadabra-tracker />
  <cryptocadabra-faq />
  <cryptocadabra-footer />
</template>

<script>
import cryptocadabraHeader from "./components/cryptocadabraHeader.vue";
import cryptocadabraHero from "./components/cryptocadabraHero.vue";
import cryptocadabraProcess from "./components/cryptocadabraProcess.vue";
import cryptocadabraInstruction from "./components/cryptocadabraInstruction.vue";
import cryptocadabraRates from "./components/cryptocadabraRates.vue";
import cryptocadabraTracker from "./components/cryptocadabraTracker.vue";
import cryptocadabraFaq from "./components/cryptocadabraFaq.vue";
import cryptocadabraFooter from "./components/cryptocadabraFooter.vue";

export default {
  name: "App",
  components: {
    cryptocadabraHeader,
    cryptocadabraHero,
    cryptocadabraProcess,
    cryptocadabraInstruction,
    cryptocadabraRates,
    cryptocadabraTracker,
    cryptocadabraFaq,
    cryptocadabraFooter,
  },
};
</script>

<style src="./main.css"></style>
