<template>
  <div id="app">
    <NavBar />
    <!-- <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div> -->
    <router-view></router-view>
  </div>
</template>

<script>
import NavBar from './components/NavBar'
export default {
  name: 'App',
  components: {
    NavBar
  }
}
</script>


<style lang="scss">
  // Global Styles
* {
    box-sizing: border-box;
    -webkit-font-smoothing: antialiased;
}

@mixin text-outline {
    font-family: Akzidensk, Arial, Helvetica, sans-serif;
    color: black;
    text-shadow:
     -2px -2px 0 white,  
      2px -2px 0 white,
      -2px 2px 0 white,
       2px 2px 0 white;
}

.text-outline {
    @include text-outline;
}

@font-face {
    font-family: Akzidensk;
    src: url(./fonts/AkzidenzGrotesk-Regular.otf) format("");
}

@font-face {
    font-family: Akzidensk Light;
    src: url(./fonts/AkzidenzGrotesk-Light.otf) format("");
}

@font-face {
    font-family: Akzidensk Bold;
    src: url(./fonts/AkzidenzGrotesk-Bold.otf) format("");
}

@font-face {
    font-family: Akzidensk Extra Bold;
    src: url(./fonts/AkzidenzGrotesk-ExtraBold.otf) format("");
}

// Colors
$color-primary: #9900ff;
$color-secondary: gold;
$color-tertiary: white;
$color-background: #000000;
$color-border: cyan;

$color-scrollbar: #454545;
$color-scrollbar-bg: #121212;
$color-scrollbar-hover: #565656;
$color-scrollbar-active: #676767;

// General
html, body {
    font-family: 'Akzidensk Light', sans-serif;
    font-weight: 200;
    font-size: 16px;
    height: 100vh;
    overflow: hidden;
    background: $color-background;
    color: white;
    
}

a {
    font-size: 1rem;
    text-decoration: none;
    user-select: none;
    color: white;
    opacity: 0.9;
    transform: opacity 0.15s;
    color: $color-secondary;

    &:hover {
        opacity: 1;
        cursor: pointer;
    }

    &:active {
        color: yellow;
    }
}

ul {
    padding: 0;
}

li {
    list-style: none;
    padding: 0 1rem;
}

img  {
    user-select: none;
    -webkit-user-drag: none;
}

h1 {
    font-family: 'Akzidensk Bold', sans-serif;
    font-weight: bold;
}

h1, h2, h3, h4, h5, h6, p {
    padding: 0px;
    margin: 0px;
}

.invert {
    filter: invert(1);
}

// Scrollbar
@mixin scrollbar {
    overflow-y: scroll;

    &::-webkit-scrollbar {
        width: 10px;
        background: $color-scrollbar-bg;
       }
     
    &::-webkit-scrollbar-thumb {
        background: $color-scrollbar;
        border-radius: 2px;
        opacity: 0.7;

        &:hover {
            background: $color-scrollbar-hover;
            opacity: 0.9;
        }

        &:active {
            background: $color-scrollbar-active;
            opacity: 1;
        }
    }
}

// Layout
.center {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    text-align: center;
    height: 85vh;
    width: 100%;
}

.flex-center {
    justify-content: center;
}

.flex-row {
    width: 100%;
    display: flex;
    flex-direction: row;
    align-items: center;
    height: auto;
}

.footer {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    width: 100vw;
    padding: 1rem;
}

.fixed-footer {
    // position: fixed;
    bottom: 15px;
    text-align: center;
    margin: 20px;
}

.gem-background-float {
    display: none;
	transform: translatey(0px);
	animation: float 3s ease-in-out infinite;

    @keyframes float {
        0% {
            transform: translatey(0px);
        }
        50% {
            transform: translatey(-20px);
        }
        100% {
            transform: translatey(0px);
        }
    }
}

</style>
