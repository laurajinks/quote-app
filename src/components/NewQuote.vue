<template>
  <div class="row">
    <form>
      <div class="col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3 formgroup">
        <label>Quote</label>
        <textarea class="form-control" rows="3" v-model="input"></textarea>
      </div>
      <div class="col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3 formgroup">
        <button class="btn btn-primary" rows="3" @click.prevent="addQuote">Add Quote</button>
      </div>
    </form>
  </div>
</template>
    
<script>
export default {
  name: "NewQuote",
  data() {
    return {
      input: ""
    };
  },
  methods: {
    addQuote() {
      this.$emit("quoteAdded", this.input);
      this.input = "";
    }
  }
};
</script>