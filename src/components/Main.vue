<template>
  <Header class="header" />
  <Section1 class="section1" :scrollTop="scrollTop" />
  <Section2 class="section2" :scrollTop="scrollTop - 700" />
  <Section3 class="section3" :scrollTop="scrollTop - 500" />
</template>

<script>

import Header from './Header.vue';
import Section1 from './sections/Section1.vue';
import Section2 from './sections/Section2.vue';
import Section3 from './sections/Section3.vue';

export default {
  name: 'Main',

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

  computed: {
    headerOpacity () {
      if (this.scrollTop < 690)
      return 0
    }
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
.header {
  transition: .3s;
  opacity: v-bind('headerOpacity');
}

.section1 {
  z-index: 1;
}

.section2 {
  z-index: 2;
}

.section3 {
  z-index: 3;
}
</style>