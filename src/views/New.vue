<template>
    <NavBar />
    <div class="Container">
        <div class="content">
            <h2>PlaceHolder: Go back to Page</h2>
            <h1 style="margin-top: 10px">Create new listing </h1>
                <div class="formsContainer">
                    <form @submit="getPostData" method="post">
                    <div class="streetName">
                        <label for="streetName">Street name*</label>
                        <input type="text" id="streetName" name="streetname" placeholder="Enter the street name..." v-model="postData.streetName">
                    </div>
                    <div class="houseNumber">
                        <span class="spanFristRow">                
                            <label for="houseNr">House number*</label>
                            <label for="additional">Addition (optional)</label>
                        </span>
                        <span class="spanSecondRow">
                            <input type="text" id="houseNr" name="housenr" placeholder="Enter your housenumber..." v-model="postData.houseNumber">
                            <input type="text" id="additional" name="additional" placeholder="e.g. A" v-model="postData.addition">
                        </span>
                    </div>
                    <div class="moreContent">
                        <label for="postalCode">Postal Code*</label>
                        <input type="text" name="postalcode" id="postalCode" placeholder="e.g. 1000 AA" v-model="postData.postalCode">
                        <label for="city">City *</label>
                        <input type="text" name="city" id="city" placeholder="Enter a city..." v-model="postData.city">
                        <label for="uploadImage">Upload Image (PNG or JPEG) *</label>
                        <input type="file" id="uploadImage" name="uploadeimage" accept="image/png, image/jpeg">
                        <label for="price">Price*</label>
                        <input type="text" id="price" name="price" placeholder="e.g. 1000" v-model="postData.price">
                    </div>
                    <div class="houseInfor">
                        <span class="spanFristRow">                
                            <label for="size">Size*</label>
                            <label for="garage">Garage*</label>
                        </span>
                        <span class="spanSecondRow">
                            <input type="text" id="size" name="size" placeholder="e.g. 60m2" v-model="postData.size">
                            <input type="number" id="garage" name="garage" placeholder="Select" v-model="postData.garage">
                        </span>
                        <span class="spanFristRow">                
                            <label for="bedrooms">Bedrooms*</label>
                            <label for="bathrooms">Bathrooms*</label>
                        </span>
                        <span class="spanSecondRow">
                            <input type="text" id="bedrooms" name="bedrooms" placeholder="Enter amount" v-model="postData.bedrooms">
                            <input type="text" id="bathrooms" name="bathrooms" placeholder="Enter amount" v-model="postData.bathrooms">
                        </span>
                        <span class="spanFristRow">                
                            <label for="constructionDate">Construction Date</label>
                        </span>
                        <span class="spanSecondRow">
                            <input type="text" id="constructionDate" name="constructionDate" placeholder="w.g. 1999" v-model="postData.constructionDate">
                        </span>
                        <span class="spanFristRow">                
                            <label for="description">Description</label>
                        </span>
                        <span class="spanSecondRow">
                            <textarea name="description" id="description" cols="50" rows="8" v-model="postData.description">Enter description</textarea>
                        </span>
                    </div>
                <input id="submitButton" type="submit" value="PUSH">
                </form>
            </div>
        </div>
    </div>
</template>

<script>
import NavBar from '@/compontents/NavBar.vue'

export default {
    name: 'New',
    components : {
        NavBar
    },
    data() {
        return {
            postData : {
                streetName: null,
                houseNumber: null,
                addition: null,
                postalCode: null,
                city: null,
                picture: null,
                price: null,
                size: null,
                garage: null,
                bedrooms: null,
                bathrooms: null,
                constructionDate: null,
                description: null
            }
        }
    },

    methods: {
        getPostData(e) {
            console.log("Data: " + this.postData)
            console.log("1: " + this.postData.streetName)
            console.log("2: " + this.postData.houseNumber)
            console.log("2: " + this.postData.addition)
            e.preventDefault();
            
        }
    }
    
}
</script>

<style scoped>
    .content {
        width: 50%; 
        display: inline-block;
        margin-left: 21%;
        margin-top: 1%;
        font-family: 'Montserrat', sans-serif;
    }

    .formsContainer {
        margin-top: 15px;
       
    }

    .streetName {
        display: grid;
        justify-content: space-between;
        height: 50px;
        margin-bottom: 50px;
    }

    .houseNumber {
        display: grid;
        margin-top: 29px;
    }

    .spanFristRow {
        justify-content: space-between;
        display: flex;
        width: 45%;
        margin-bottom: 5px;
    }

    .spanSecondRow {
        width: 49%;
        display: flex;
        justify-content: space-between;
    }

    .moreContent {
        display: grid;
        justify-content: space-between;
        height: 80%;
      
    }

    #uploadImage {
        border: 1px solid #ccc;
        display: inline-block;
        padding: 6px 12px;
        cursor: pointer;
        text-align: center;
    }

    label {
        margin-bottom: 20px;
    }

    input {
        margin-bottom: 20px;
        border: none;
        background-color: white;
        height: 40px;
        padding-left: 5px;
        border-radius: 10px;
             font-family: 'Montserrat', sans-serif;
    }

    textarea {
        background-color: white;
        border: none;
        padding: 20px 15px;
        border-radius: 10px;
        font-family: 'Montserrat', sans-serif;
    }

    #submitButton {
        text-align: center;
        margin-top: 15px;
        margin-left: 220px;
        width: 20%;
        background-color: #EB5440;
        color: white;
    }
    
</style>