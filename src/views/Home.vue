<template>
  <div></div>
</template>

<script>

export default {
  name: 'Home',
  components: {

  }
}
</script>

<style lang="scss" scoped>

.gem-background-wrapper {
    position: fixed;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: 100vw;
    height: 32vmax;
    pointer-events: none;
    user-select: none;
    -webkit-user-drag: none;
    // filter: blur(4px);

    .gem-background {
        display: block;
        width: 100vw;
        height: 100vh;
        object-fit: contain;
        z-index: -1;
        opacity: 0.15;
        pointer-events: none;
        user-select: none;
        -webkit-user-drag: none;
        padding: 30px;
            
    }

}

</style>
