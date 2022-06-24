<template>
<div class="container">
    <div class="firstRow">
        <h1>Houses</h1>
        <input type="search" id="search" placeholder="Search for...">
    </div>
    <div class="secondRow">
        <router-link class="newHouseButton" to="/new">+ New House</router-link>
        <div class=prsi>
        <a href="">Price</a>
        <a href="">Size</a>
        </div>
    </div>
</div>
    
</template>

<script>
export default {
    name: 'TopBar',        
}
</script>

<style scoped>
    
    .container {
        height: 150px;
        width: 100%;
        display: flex;
        font-family: 'Open Sans', sans-serif;
    

    }

    .firstRow {
        margin-top: 10px;
        margin-left: 20%;
      
    }

    .secondRow {
        margin-top: 8px;
        margin-left: 20%;
        display: grid;

    }

    .prsi {
        display: flex;
        padding: 3%;
        background-color: rgb(235, 84, 84);
        height: 3em;
        width: 11em;
        padding-top: 10px;
        text-align: center;
        border-radius: 10px;
    }

    #search {
        border: 2px solid #999;
        border-radius: 4px;
        font-size: 1.2em;
        width: 20em;
        height: 2em;
        transition: width 0.5s ease-in-out;
        margin-top: 40px;
    }

    #suche:focus {
        font-size: 1.5em;
        width: 50%;
    }

    .newHouseButton {
        background-color: rgb(235, 84, 84);
        height: 3em;
        width: 11em;
        padding-top: 10px;
        text-align: center;
        border-radius: 10px;
    }
</style>