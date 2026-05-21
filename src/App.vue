<script>
import NavBar from './components/NavBar.vue';
import Menu from './components/Menu.vue';
import Story from './components/Story.vue';

export default {
  components: {
    Menu,
    NavBar,
    Story,

  },
  data() {
    return {
      currentPage: 'Menu'
    }
  },
  methods: {
    changePage(page) {
      this.currentPage = page;
    }
  }
}
</script>

<template>
  <NavBar @goTo="changePage" :activePage="currentPage" />
  <Menu v-if="currentPage === 'Menu'"/>
  <Story v-if="currentPage === 'Story'" />

</template>
