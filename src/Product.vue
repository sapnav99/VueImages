<template>
    <div>
    <input type="text" v-model="input" placeholder="Search images..." />
    
    <div class="Images">
        <div class="ImagePanel" v-for="content in contents" :key="content.id">
            <img :src="content.url" @click="changeSource" />
            {{content.title}}
        </div>
    </div>
</div>

</template>
<script>
import axios from 'axios';


export default {
    name: 'ProductImage',
    data() {
        return {
            contents: null,
        }
    },
    mounted() {
        axios
            .get("https://jsonplaceholder.typicode.com/photos")
            .then(response => (this.contents = response.data))
    },
   
    }

</script>
<style>
.Images {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(20rem, 1fr));
    grid-gap: 1rem;
    max-width: 80rem;
    margin: 5rem auto;
    padding: 0 5rem;
}

.ImagePanel img {
    width: 100%;
    height: 15vw;
    object-fit: cover;
    border-radius: 0.75rem;
}

</style>