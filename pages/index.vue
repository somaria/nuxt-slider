<template>
  <no-ssr placeholder="Loading...">
    <div class="container items-center mx-64">
      <carousel :data="carouseldata"></carousel>
    </div>
  </no-ssr>
</template>

<script>
export default {
  data() {
    return {
      carouseldata: [
        {
          id: 1,
          message: "First message",
          content(createElement, content) {
            return createElement("img", {
              attrs: {
                src: require("~/assets/japan.jpeg")
              }
            });
          }
        },
        {
          id: 2,
          message: "Any message",
          content(createElement, content) {
            return createElement("img", {
              attrs: {
                src: require("~/assets/newyork.jpeg")
              }
            });
          }
        }
      ]
    };
  }
};
</script>

<style>
/* Sample `apply` at-rules with Tailwind CSS
.container {
@apply min-h-screen flex justify-center items-center text-center mx-auto;
}
*/
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

.example-slide {
  align-items: center;
  background-color: #666;
  color: #999;
  display: flex;
  font-size: 1.5rem;
  justify-content: center;
  min-height: 10rem;
}
</style>
