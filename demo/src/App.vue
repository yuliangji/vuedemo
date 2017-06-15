<template>
  <div id="app">
    <c-header></c-header>
    <c-content>
      <img src="./assets/logo.png" class="logo-img">
    </c-content>
    <c-highlights></c-highlights>
    <c-sponsors></c-sponsors>
    <c-footer></c-footer>
  </div>
</template>

<script>
import header from './components/header/header.vue';
import content from './components/content/content.vue';
import highlights from './components/highlights/highlights.vue';
import sponsors from './components/sponsors/sponsors.vue';
import footer from './components/footer/footer.vue';
export default {
  components: {
    'c-header':header,
    'c-content':content,
    'c-highlights':highlights,
    'c-sponsors':sponsors,
    'c-footer':footer
  }
}
</script>

<style>
</style>
