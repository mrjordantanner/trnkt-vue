<template>
			<div>
				<div class='home-container'>
					<img class='gem-background-float invert' src='../assets/diamond.svg' />
					<div class='logo text-outline'>TRNKT</div>
					<p class='description'>
						Discover a wide variety of crypto <a href='https://en.wikipedia.org/wiki/Non-fungible_token' target='_blank' ><strong>NFT</strong></a> artwork.
						Use the Explore button to display random NFT's from the Opensea API, click or tap to view them in detail, and save to your Collection for later viewing. <br></br>
					</p>
					<router-link to='/explore'>
						<button @click="$emit('randomize-offset')" class='button outline-secondary enter'>
							E X P L O R E
						</button>
					</router-link>
					<footer class='fixed-footer'>
						<p>Powered by <a href='https://opensea.io/' target='_blank'><strong>Opensea.io</strong></a></p>
					    <p>Copyright &copy; 2021 -- <a href='https://github.com/mrjordantanner' target='_blank'><strong>Jordan Smith Digital</strong></a></p>
					</footer>
				</div>
			</div>
</template>

<script>

export default {
  name: 'Home',
  components: {

  },
  mounted() {

  }
}
</script>

<style lang="scss" scoped>
.home-container {
    height: 93vh;
    width: auto;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    background: black;

    .logo {
        font-size: 14rem;
        font-weight: bold;
        z-index: 1;
        border-bottom:#7f00d3 10px solid;
    }
    
    .description {
        color: lightgray;
        width: 70vw;
        word-wrap: normal;
        line-height: 1.75rem;
        text-align: center;
        z-index: 1;
        padding: 1rem;
        margin: 1rem;
    }
}


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
