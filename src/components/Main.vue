<template>
    <Header class="header" />
    <Section1 class="section1" :scrollTop="scrollTop" />
    <Section2 class="section2" :scrollTop="scrollTop - 700" />
    <Section3 class="section3" :scrollTop="scrollTop - 500" />
    <Section4 class="section4" :scrollTop="scrollTop - 300" />
    <Section5 class="section5" />
    <Footer class="footer" />
</template>

<script>

import Header from './Header.vue';
import Section1 from './sections/Section1.vue';
import Section2 from './sections/Section2.vue';
import Section3 from './sections/Section3.vue';
import Section4 from './sections/Section4.vue';
import Section5 from './sections/Section5.vue';
import Footer from './Footer.vue'

export default {
  name: 'Main',

  components: {
    Header,
    Section1,
    Section2,
    Section3,
    Section4,
    Section5,
    Footer
  },

  mounted() {
    window.scrollTo(0, 0);
    document.addEventListener('scroll', this.onScroll);
  },

  computed: {
    headerOpacity() {
      if (this.scrollTop < 688)
        return 0
    }
  },

  beforeUnmount() {
    document.removeEventListener('scroll', this.onScroll);
  },

  methods: {
    onScroll() {
      this.scrollY = window.scrollY
      this.scrollTop = window.scrollY / window.outerHeight * 100
    }
  },

  data() {
    return {
      scrollTop: 0
    }
  }
}
</script>

<style scoped lang="scss">
.header {
  transition: .3s;
  opacity: v-bind('headerOpacity');
}

// .section1 {
//   z-index: 1;
// }

// .section2 {
//   z-index: 2;
// }

// .section3 {
//   z-index: 3;
// }
</style>