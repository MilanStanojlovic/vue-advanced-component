<template>
  <div class="container">
    <div class="row">
      <div class="coll-xs-12">
        <app-quote>
          <h1 slot="title">{{ quoteTitle }}</h1>
          <p slot="content">A wonderful quote</p>
        </app-quote>
      </div>
    </div>
  </div>
</template>

<script>
import Quote from "./components/Quote";
export default {
  components: {
    "app-quote": Quote
  },

  data: () => {
    return {
      quoteTitle: "The Quote"
    };
  }
};
</script>

<style>
h1 {
  color: blue;
}
</style>
