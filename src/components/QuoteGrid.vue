<template>
  <div class="row">
    <Quote
      v-for="(quote, index) in quotes"
      :key="index"
      :quote="quote"
      @click.native="deleteQuote(index)"
    />
  </div>
</template>
    
<script>
import Quote from "./Quote";
export default {
  name: "QuoteGrid",
  components: {
    Quote
  },
  props: ["quotes"],
  methods: {
    deleteQuote(index) {
      this.$emit("quoteDeleted", index);
    }
  }
};
</script>