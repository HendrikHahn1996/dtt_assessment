<template>
    <NavBar />
    <div class="Container">
        <dir class="content">
            <h1>PlaceHolder: Go back to Page</h1>

        </dir>
    </div>
</template>

<script>
import NavBar from '@/compontents/NavBar.vue'

export default {
    name: 'New',
    components : {
        NavBar
    }
    
}
</script>

<style scoped>
    .content {
        width: 50%; 
        display: grid;
        margin-left: 21%;
        margin-top: 1%;
        background-color: red;
    }
    
</style>