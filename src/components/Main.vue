<template>
  <Header />
  <Section1 :scrollTop="scrollTop" />
  <Section2 :scrollTop="scrollTop - 450" />
  <Section3 :scrollTop="scrollTop - 500" />
</template>

<script>

import Header from './Header.vue';
import Section1 from './sections/Section1.vue';
import Section2 from './sections/Section2.vue';
import Section3 from './sections/Section3.vue';

export default {
  components: {
    Header,
    Section1,
    Section2,
    Section3
  },

  mounted () {
    window.scrollTo(0, 0);
    document.addEventListener('scroll', this.onScroll);
  },

  beforeUnmount () {
    document.removeEventListener('scroll', this.onScroll);
  },

  methods: {
    onScroll () {
      this.outerHeight = window.outerHeight
      this.scrollY = window.scrollY
      this.scrollTop = window.scrollY / window.outerHeight * 100
    }
  },

  data () {
    return {
      scrollTop: 0,
      scrollY: 0,
      outerHeight: 0
    }
  }
}
</script>

<style scoped lang="scss">
</style>