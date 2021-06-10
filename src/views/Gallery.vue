<template>
    <div class='gallery-wrapper' >

        <!-- <div class='gem-background-wrapper'>
            <img clasclasssName='gem-background invert' src='../assets/diamond.svg' alt='diamond'/>
        </div> -->

        <div :key="asset.id" v-for="asset in assets" class='gallery-container'>
            <Card :asset="asset" />
        </div>

    </div>
</template>

<script>
// Displays up to 50 NFT's randomly selected from the OpenSea API

import Card from '../components/Card'

export default {
  name: 'Gallery',
  data() {
      return {
          assets: [
              {

              },
              {
                  
              },
          ]
      }
  },
  components: {
      Card
  },

}
</script>


<style lang="scss" scoped>

@mixin scrollbar {
    overflow-y: scroll;

    &::-webkit-scrollbar {
        width: 10px;
        background: #121212;
       }
     
    &::-webkit-scrollbar-thumb {
        background: #454545;
        border-radius: 2px;
        opacity: 0.7;

        &:hover {
            background: #565656;
            opacity: 0.9;
        }

        &:active {
            background: #676767;
            opacity: 1;
        }
    }
}

.gallery-wrapper {
    display: flex;
    align-items: center;

    flex-direction: column;
    height: 100vh;
    @include scrollbar;
    background-color: black;
    color: white;

    .gallery-container {
        margin-top:100px;
        width:100%;
        height:auto;
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
        padding: 0 1rem;
    }
}

.invert {
    filter: invert(1);
}

</style>