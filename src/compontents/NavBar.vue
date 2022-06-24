<template>
<div class="nav">
    <div class="container">
        <img src="@/assets/dtt_logo.png" alt="Logo">
        <div class="routerLinks">
        <router-link to="/">Home</router-link>
        <router-link to="/new">About</router-link>
        <router-view />
        </div>
    </div>
</div>
    
</template>

<script>
export default {
    name: 'NavBar'
}
</script>

<style scoped>

.nav {
    background-color: white;
    width: 100%;
    height: 80px;
     font-family: 'Open Sans', sans-serif;
}

img {
    width: 8%;
    height: 40px;
    margin-top: 15px;
}

.container {
    margin-left: 20%;
    background-color: white;
    display: flex;
    padding-left: 20px;
}

.routerLinks {
   margin-left: 35px;
   margin-top: 25px;
   height: 10px;
}


</style>