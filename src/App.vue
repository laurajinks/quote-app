<template>
  <div id="app">
    <Header :maxQuotes="maxQuotes" :quoteCount="quotes.length"/>
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
import Header from "./components/Header";
import NewQuote from "./components/NewQuote";
import QuoteGrid from "./components/QuoteGrid";

export default {
  name: "app",
  components: { Header, NewQuote, QuoteGrid },
  data() {
    return {
      quotes: ["Just a Test Quote"],
      maxQuotes: 10
    };
  },
  methods: {
    addQuote(quote) {
      if (this.quotes.length < this.maxQuotes) {
        this.quotes.push(quote);
      } else {
        return alert(
          "You can only have 10 quotes! Please delete a quote before adding a new one."
        );
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
