<template>
   <div class="companies-section">
        <div class="container">
            <div class="small-bold-text companies-header">The world’s best companies rely on UsabilityHub to make better design decisions.</div>
            <div class="logos flex" >
                
                <img class="logo" v-for="(item , i) in image" :key="i" :src="item.url" >
                
                
            </div>
        </div>
    </div>
</template>

<script>
import img1 from '../assets/asset 3.png';
import img2 from '../assets/asset 4.png';
import img3 from '../assets/asset 5.png';
import img4 from '../assets/asset 6.png';
import img5 from '../assets/asset 7.png';
import img6 from '../assets/asset 8.svg';
import img7 from '../assets/asset 9.png';
export default {
    data(){
        return{
            image:[{url:img1},{url:img2},{url:img3},{url:img4},{url:img5},{url:img6},{url:img7}]
        }
    }
}
</script>

<style>
.companies-header{
    text-align: center;
    margin-block: 30px;
    color: var(--primary-text-color);
}
.logos{
    justify-content: space-evenly;
    flex-wrap: wrap;
    gap: 20px;
}
.logo{
    height: 46px;
}
</style>