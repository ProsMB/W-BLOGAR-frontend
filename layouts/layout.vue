<template>
  <section>
      <navigation-bar></navigation-bar>
      <nuxt class=""/>
      <!-- bg-[#f8fafc] -->
      <footer-bar></footer-bar>

  </section>
</template>

<script>
import footer_bar from '~/components/footer_bar.vue';
import navigation_bar from '~/components/navigation_bar.vue';
export default {
    components:{'navigation-bar':navigation_bar,'footer-bar':footer_bar},

}
</script>

<style>

</style>