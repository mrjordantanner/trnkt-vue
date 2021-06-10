<template>
    <div>
        <div v-show="showNavBar" class="navbar-container">
            <router-link to="/" class="nav-link">TRNKT</router-link>
            <router-link to="/explore" class="button outline-primary" @click="$emit('randomize-offset')">E X P L O R E</router-link>
            <router-link to="/collection" class="button outline-secondary" v-show="showCollectionButton">C O L L E C T I O N</router-link>  
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
            showNavBar: true
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

    .button {
    // pointer-events: auto;
    z-index: 100;
    padding: 0.35rem 1rem;
    margin: 0 1.5rem;
    font-weight: bold;
    font-size: 1rem;
    transition: all 0.15s;
    background: transparent;
    user-select: none;

        &:hover {
            cursor: pointer;
        }
    }

    .outline-primary {
        height: 36px;
        color: gold;
        border: 3px solid gold;

        &:hover {
            background: gold;
            color: black;
            
        }
    }

    .outline-secondary {
        height: 36px;
        color: violet;
        border: 3px solid violet;

        &:hover {
            background: violet;
            color: black;
        }
    }

}
</style>