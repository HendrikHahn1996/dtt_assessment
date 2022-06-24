<template>
<div class="listHouses">
    <div class="card" v-for="house in houses" :key="house.id">
        <div class="imageHouse">{{ house.image + " image"}} </div>
            <div class="description">
                <div class="price">{{ house.price + " €"}}</div>
                <div class="location">
                    {{ house.location.street + " "}} 
                    {{ house.location.city + " "}} 
                    {{ house.location.zip}}
                </div>
                <div class="roomsSize">
                <img src="@\assets\ic_bed@3x.png" alt="bed_icon">
                <div class="rooms">{{ house.rooms.bedrooms}}</div>
                <img src="@\assets\ic_bath@3x.png" alt="bath_icon">
                <div class="rooms">{{ house.rooms.bathrooms}}</div>
                <img src="@\assets\ic_size@3x.png" alt="size_icon">
                <div class="size">{{ house.size + " m2"}}</div>
                </div>
       
                
            </div>
    </div>
</div>
</template>

<script>
import axios from 'axios';

export default {
    name: 'HouseCard',
    components: {
        
    },

    data() {
        return {
            houses : [],
        }
    },

    async created() {
        await axios.get('https://api.intern.d-tt.nl/api/houses', {
            headers : {
                'X-Api-Key' : "Kda4o9W51QjAzb2GLeDpNwuEYJmrHUsM"
            }
        })
        .then(res => res.data)
        .then(data=> {
            this.houses = data;
            //console.log(data)
            }
        )
        .catch(error => console.log(error));
    },

    
}
        
</script>

<style scoped>

.listHouses {
    background-color: rgb(246, 246, 246);
    margin-top: 0px;
}

.card {
    height: 150px;
    width: 50%; 
    background-color: white;
    margin-bottom: 15px; 
    padding: 10px 20px;
    display: flex; 
    border-radius: 5px;
    margin-left: 20%;
    margin-top: 20px;
    font-family: 'Open Sans', sans-serif;

}

.description {
    height: 130px;
    display: grid;

    margin-left: 15%;
    justify-content: space-between;
}

.imageHouse {
    height: 40%;
    width: 5%;
    display: flex;
    justify-content: flex-start;

}

.rooms {
    padding: 0px;
}

.location {
    display: flex;
}

.roomsSize {
    display: flex;
}

img {
    height: 20px;
    padding-right: 5px;
    margin-left: 15px;

}
    
</style>