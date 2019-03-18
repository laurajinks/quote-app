<template>
  <div class="col-sm6 col-md4 col-lg-3">
    <div class="panel panel-default">
      <h2 class="quote">{{ quote }}</h2>
    </div>
  </div>
</template>

<script>
export default {
  name: "Quote",
  props: ["quote"]
};
</script>

<style>
.panel {
  font-family: "Arizonia", cursive;
  font-size: 24px;
  color: #6e6e6e;
}

.quote {
  cursor: pointer;
}

.quote:hover {
  background: #ffe2e2;
}
</style>

