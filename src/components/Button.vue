<template>
    <router-link to="/explore" class="button outline-primary">{{ text }}</router-link> 
</template>

<script>
export default {
    name: 'Button',
    props: {
        text: String,
    },
    methods: {
        onClick() {
            this.$emit('btn-click')
        }
    }
}
</script>

<style lang="scss" scoped>
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
</style>