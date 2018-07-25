<template>
    <div class="slide">
        <img :src="image" alt="">
    </div>
</template>

<script>
export default {
    props: {
        image: {
            type: String
        }
    },
    data() {
        return {

        }
    }
}
</script>

<style scoped>
    img {
        max-width: 100%;
        width: 100%;
        height: auto;
    }

    .slide {
        display: inline-block;
    }
</style>