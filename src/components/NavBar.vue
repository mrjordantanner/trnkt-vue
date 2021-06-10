<template>
    <div>

        <div class="navbar-container">
            <router-link to="/" class="nav-link">TRNKT</router-link>
            <Button @btn-click="$emit('btn-click')" class="button outline-primary" text="EXPLORE"/>
            <Button @btn-click="$emit('btn-click')" v-show="showCollectionButton" class="button outline-secondary" text="COLLECTION" />
        </div>
    </div>
</template>

<script>
import Button from './Button'
export default {
    name: 'NavBar',
    data() {
        return {
            showCollectionButton: true,
        }
    },
    components: {
        Button
    },
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
        opacity: 0.8;
        transition: all 0.1s;

        &:hover {
            opacity: 0.9;
        }

        &:active {
            opacity: 1;
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