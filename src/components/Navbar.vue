<template>
    <div class="navbar">
        
        <ul>
            <li><router-link to="/">Home</router-link></li>
            <li><router-link to="/member">Member</router-link></li>
            <!-- <li><router-link to="/">Home</router-link></li>
            <li><router-link to="/">Home</router-link></li> -->
        </ul>
        
    </div>
</template>

<script>
export default {
    name: 'Navbar',
    data () {
        return {
            msg: 'Navbar ...'
        }
    }
}
</script>

<style scoped>
    ul {
        width: 100%;
        margin: 0;
        padding: 0;
        line-height: 60px;
    }

    ul li {
        display: inline-block;
        padding: 0 2em 0 2em;
    }

    ul li a {
        text-decoration: none;
        color: #fff;
        font-size: 1em;
    }
</style>
