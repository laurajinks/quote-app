<template>
  <div id="app">
    <NewQuote @quoteAdded="addQuote"/>
    <QuoteGrid :quotes="quotes" @quoteDeleted="deleteQuote"/>
    <div class="row">
      <div class="col-sm-12 text-center">
        <div class="alert alert-info">Click on a Quote to Delete</div>
      </div>
    </div>
  </div>
</template>

<script>
import NewQuote from "./components/NewQuote";
import QuoteGrid from "./components/QuoteGrid";

export default {
  name: "app",
  components: { NewQuote, QuoteGrid },
  data() {
    return {
      quotes: ["Just a Test Quote"],
      maxQuotes: 10
    };
  },
  methods: {
    addQuote(quote) {
      if (this.quotes.length < 10) {
        this.quotes.push(quote);
      }
    },
    deleteQuote(index) {
      this.quotes.splice(index, 1);
    }
  }
};
</script>

<style>
</style>
