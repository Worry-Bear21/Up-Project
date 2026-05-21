<script>

export default {
    data() {
        return {
            activePage: 'Menu'
        }
    },
    methods: {
        navigate(page) {
            this.$emit('goTo', page);
            this.activePage = page;
        }
    }
}
</script>

<template>
    <nav id="NavBar">
        <div id="NavCon">
            <div id="NavMenu">
                <h1 @click="navigate('Menu')" id="NavText">
                    MENU</h1>
                <h1 @click="navigate('Story')" id="NavText">
                    OUR STORY</h1>
                <h1 @click="navigate('Catering')" id="NavText">
                    CATERING</h1>
            </div>
            <div>
                <img id="Logo" src="../assets/images/maple.webp" alt="">
            </div>
            <div id="NavMenu" class="flex gap-5 mt-5">
                <h1 id="NavText">
                    GIFT CARDS</h1>

                <h1 id="NavText">
                    SHOP</h1>
                <h1 id="Btn">
                    SIGN IN</h1>

            </div>
        </div>

    </nav>

</template>
