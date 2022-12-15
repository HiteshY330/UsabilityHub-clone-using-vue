<template>
  <nav>
        <div class="container main-nav flex">
            <a href="" class="company-logo">
                <img :src="companyLogo" alt="company logo" >
            </a>
            <div class="nav-links" :class="toggleactive" id="nav-link">
                <ul class="flex">
                    <li v-for="navdata in nav" :key="navdata"><a href="#" class="hover-links">{{navdata}}</a></li>
        
                    <li><a href="#" class="hover-links secondary-button">Sign in</a></li>
                    <li><a href="#" class="hover-links primary-button"> Sign up</a></li>
                </ul>
            </div>
            <a href="#" id="nav-toggle" @click="toggle()" class="nav-toggle hover-links">
                <i class="fa-solid fa-bars"></i>
            </a>
        </div>
    </nav>
</template>

<script>
import logo from '../assets/asset 1.png';
export default {
    data(){
        return{
            nav:['Product','Customer','Pricing','Resources'],
            companyLogo:logo,
            toggleactive:'',
            change:true,
        }
    },
    methods:{
        toggle(){
            //console.log('toggle')
            //this.toggleactive = active;
            this.change = !this.change;
            if(this.change === true){
                this.toggleactive = 'active';
            }else{
                this.toggleactive ='';
            }
        }
    }
}
</script>

<style>
.main-nav{
    margin-top: 20px;
    justify-content: space-between;
}
.company-logo img{
    width: 200px;
}
.nav-links{
    flex-basis: 730px;
}
.nav-links ul{
    justify-content: end;
    gap: 40px;    
}
.hover-links{
    color: var(--primary-text-color);
    transition: 0.2s ease-out;
}
.hover-links:hover{
    color: var(--accent-color);

}
.nav-toggle{
    display: none;
}
/* header section*/

header{
    padding: 50px var(--padding-inline-section);
}
.header-section{
    justify-content: center;
    gap: 50px;
}
.left-header{
    max-width: 40vw;
}
.left-header h1{
    margin-top: 20px;
}
.get-started-btn{
    margin-top: 20px;
}
.right-header img{
    width: 100%;
}

</style>
