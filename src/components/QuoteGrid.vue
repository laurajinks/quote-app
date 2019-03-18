<template>
  <div class="row">
    <Quote v-for="(quote, index) in quotes" :key="index" :quote="quote"/>
  </div>
</template>
    
<script>
import Quote from "./Quote";
export default {
  name: "QuoteGrid",
  components: {
    Quote
  },
  props: ["quotes"]
};
</script>