<template>
    <div v-show="showNavBar" class="navbar-container">

        <router-link to="/">
            <a class="nav-link" @click="hideNavBar">TRNKT</a>
        </router-link>

        <router-link to="/explore" >
            <button class="button outline-primary" @click="randomizeOffset(); displayCollectionButton()">E X P L O R E</button>
        </router-link>

        <router-link to="/collection">
            <button class="button outline-secondary" v-show="showCollectionButton" @click="hideCollectionButton">C O L L E C T I O N</button>  
        </router-link>  

    </div>
</template>

<script>

export default {
    name: 'NavBar',
    data() {
        return {
            showCollectionButton: true,
            showNavBar: true
        }
    },
    methods: {
        randomizeOffset() {
            this.$emit('randomize-offset')
        },
        displayCollectionButton() {
            this.showCollectionButton = true
        },
        hideCollectionButton() {
            this.showCollectionButton = false
        },
        hideNavBar() {
            // this.showNavBar = false
        }
    }

}
</script>

<style lang="scss" scoped>
.navbar-container {
    position: fixed;
    top: 0px;
    display:flex;
    flex-direction: row;
    justify-content: flex-start;
    align-items: center;
    width: 100vw;
    height: 70px;
    z-index: 900;
    padding: 0 50px;
    border-bottom: 1px solid white;

    .nav-link {
        font-family: 'Akzidensk', sans-serif;
        pointer-events: auto;
        color: white;
        font-size: 1.75rem;
        font-weight: bold;
        opacity: 0.9;
        transition: all 0.1s;

        &:hover {
            opacity: 1;
        }

        &:active {
            color: gold;
        }
    }

    .navbar-blur {
        position: fixed;
        z-index: -1;
        width: 100vw;
        height: 70px;
        top: 0px;
        margin: 0 0 0 0px;
        background: black;
        opacity: 0.7;
        -webkit-backdrop-filter: blur(10px);
        backdrop-filter: blur(10px);
        border-bottom: 2px white solid;
    }

    li {
        display: inline;
    }

}
</style>