<template>
  <div id="app">
    <QuoteGrid :quotes="quotes"/>
  </div>
</template>

<script>
import QuoteGrid from "./components/QuoteGrid";
export default {
  name: "app",
  components: { QuoteGrid },
  data() {
    return {
      quotes: ["Just a Test Quote"],
      maxQuotes: 10
    };
  }
};
</script>

<style>
</style>
