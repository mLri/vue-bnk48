<template>
    <div class="head">
        <router-link to="/">Home</router-link>
        <router-link to="/member">Member</router-link>
    </div>
</template>

<script>
export default {
    name: '',
    data () {
        return {
            msg: ''
        }
    }
}
</script>

<style scoped>
    .head {
        width: 100%;
        display: block;
        background-color: orange;
        min-height: 60px;
    }
</style>