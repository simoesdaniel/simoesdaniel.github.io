<template>
  <div class="flex justify-center items-center py-6 max-w-3xl mx-auto px-4">
    <div>
      <Logo />
      <h1 class="text-2xl py-6 text-center">
        Hey there 👋 I'm Luís!
      </h1>
      <About />
      <hr class="my-6" />
      <Social />
    </div>
  </div>
</template>

<script>
import About from "../components/About.vue";
import Social from "../components/social/Social.vue";
export default {
  components: { Social, About }
};
</script>
