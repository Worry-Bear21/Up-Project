<script>
export default {
  data() {
    return {
      activePage: 'Menu'
    }
  },

  methods: {
    navigate(page) {
      this.$emit('goTo', page)
      this.activePage = page
    }
  }
}
</script>

<template>
  <nav id="NavBar">

    <div id="NavCon">

      <!-- LEFT -->
      <div class="NavMenu">

        <h1
          @click="navigate('Menu')"
          :class="['NavText', activePage === 'Menu' ? 'active' : '']"
        >
          MENU
        </h1>

        <h1
          @click="navigate('Story')"
          :class="['NavText', activePage === 'Story' ? 'active' : '']"
        >
          OUR STORY
        </h1>

        <h1
          @click="navigate('Catering')"
          :class="['NavText', activePage === 'Catering' ? 'active' : '']"
        >
          CATERING
        </h1>

      </div>

      <!-- LOGO -->
      <div>
        <img id="Logo" src="../assets/images/maple.webp" alt="">
      </div>

      <!-- RIGHT -->
      <div class="NavMenu">

        <h1 class="NavText">
          GIFT CARDS
        </h1>

        <h1 class="ShopText">
          SHOP
        </h1>

        <h1 class="NavText">
          ORDER ONLINE
        </h1>

        <button id="Btn">
          VISIT US
        </button>

      </div>

    </div>

  </nav>
</template>