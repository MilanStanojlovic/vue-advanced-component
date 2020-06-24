<template>
  <div class="container">
    <div class="row">
      <div class="coll-xs-12">
        <button @click="selectedComponent = 'app-quote'">Quote</button>
        <button @click="selectedComponent = 'app-author'">Author</button>
        <button @click="selectedComponent = 'app-new'">New</button>
        <hr />
        <p>{{ selectedComponent }}</p>
        <keep-alive>
          <component :is="selectedComponent">
            <p slot="content">Default content</p>
          </component>
        </keep-alive>
        <!-- <app-quote>
          <h1 slot="title">{{ quoteTitle }}</h1>
          <p slot="content">A wonderful quote</p>
        </app-quote> -->
        <hr />
      </div>
    </div>
  </div>
</template>

<script>
import Quote from "./components/Quote";
import Author from "./components/Author";
import New from "./components/New";

export default {
  components: {
    "app-quote": Quote,
    "app-author": Author,
    "app-new": New
  },

  data: () => {
    return {
      quoteTitle: "The Quote",
      selectedComponent: "app-quote"
    };
  }
};
</script>

<style>
h1 {
  color: blue;
}
</style>
