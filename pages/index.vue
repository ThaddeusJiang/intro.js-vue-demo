<template>
  <div class="container">
    <div>
      <Logo />
      <h1 class="title">
        intro.js-vue-demo
      </h1>
      <section>
        <input type="text" name="name" />
        <button id="btn-say" @click="say">say hi</button>
      </section>
    </div>
  </div>
</template>

<script>
import introJs from "intro.js";

export default {
  mounted() {
    introJs()
      .setOptions({
        steps: [
          // {
          //   title: "Welcome",
          //   intro: "Hello World! 👋"
          // }
          {
            element: document.querySelector("input[name='name']"),
            intro: "Typing your name"
          },
          {
            title: "Step 2",
            element: document.querySelector("#btn-say"),
            intro: "Clicking button"
          }
        ]
      })
      .start();
  }
};
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont,
    "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
