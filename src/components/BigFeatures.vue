<template>
  <div>
    <section class="big-features-section">
        <div class="container flex big-feature-container" v-for="(items, i) in bigfeature" :key="i">
            <div class="feature-img">
                <img :src="items.img" alt="design">
            </div>
            <div class="feature-desc flex">
                <h4>{{items.h4}}</h4>
                <h3>{{items.h3}}</h3>
                <p>{{items.p}}</p>
            </div>
        </div>
    </section>
    
    <section class="example-section">
        <div class="container">
            <div class="example-header flex">
                <h2>One platform, endless possibilities</h2>
                <a href="#" class="secondary-button">See all example  <i class="fa-solid fa-arrow-right"> </i></a>
            </div>
            <div class="example-area flex">
                <a href="#" class="example-card" v-for="(exp, i) in examplecard" :key="i">
                    <h3 class="card-text" >{{exp}}</h3>
                </a>
            </div>
        </div>
    </section>

    <section class="cta-section">
        <div class="container flex cta-container">
            <h2>Start testing today</h2>
            <p>Take the guesswork out of design decisions</p>
            <a href="#" class="primary-button">Get Started</a>
        </div>
    </section>

    <footer>
        <div class="container flex footer-container">
            <a href="#" class="company-logo">
                <img :src="logo" alt="company logo" >
            </a>
            <div class="link-col flex" v-for="links in footerlinks" :key="links.heading">
                <h4>{{links.heading}}</h4>
                <a href="#" class="hover-links" v-for="(item, i) in links.link" :key="i">{{item}}</a>
            </div>
            
        </div>
    </footer>

    <div class="sub-footer">
        <div class="container subfooter-container flex" >
                <a href="#" class="hover-links" v-for="(item, i) in subfooter " :key="i">{{item}}</a>
                <a href="#" class="hover-links"><i class="fa-brands fa-square-facebook"></i></a>
                <a href="#" class="hover-links"><i class="fa-brands fa-twitter"></i></a>
                <a href="#" class="hover-links"><i class="fa-brands fa-linkedin"></i></a>
                <a href="#" class="hover-links"><i class="fa-brands fa-youtube"></i></a>
        </div>
    </div>
  </div>
</template>

<script>
import image from '../assets/asset 18.png';
import image1  from '../assets/asset 21.png';
import image2 from '../assets/asset 24.png';

import companylogo from '../assets/asset 1.png';
export default {
    data(){
        return{
            bigfeature:[
                {
                    img:image,
                    h4:'Effortless validation for',
                    h3:'Design professionals',
                    p:'Test interfaces, interaction flows, iconography and more, to help you create intuitive and delightful experiences for your users.'
                },
                {
                    img:image1,
                    h4:'Effortless validation for',
                    h3:'Design professionals',
                    p:'Test interfaces, interaction flows, iconography and more, to help you create intuitive and delightful experiences for your users.'
                },
                {
                    img:image2,
                    h4:'Effortless validation for',
                    h3:'Design professionals',
                    p:'Test interfaces, interaction flows, iconography and more, to help you create intuitive and delightful experiences for your users.'
                },
            ],
            examplecard:[
                'Can users complete a task in my software interface?',
            'Can users complete a task in my software interface?',
            'Can users complete a task in my software interface?',
            'Can users complete a task in my software interface?',
            ],
            logo:companylogo,
            footerlinks:[
                {
                    heading:'Product',
                    link:['Overview','Pricing','UsabilityHub panel','Customers','Status page','Testing']
                },
                {
                    heading:'Methodologies',
                    link:['Card','Sorting','Testing','Help center','Contact','Careers']
                },
                {
                    heading:'Resources',
                    link:['Blog','Example','Testing','First click test','Design',' Five click test']
                }
            ],
            subfooter:['Privacy policy','Terms & conditions','Security information']
        }
    }
}
</script>

<style>
.big-features-section{
    padding: 30px var(--padding-inline-section) 0;

}
.big-feature-container{
    gap: 50px;
}
.big-feature-container:nth-child(2){
    flex-direction: row-reverse;
}
.feature-img img{
    width: 100%;
}
.feature-desc{
    flex-direction: column;
    /*align-items: flex-start;*/
    text-align: center;
}

/* example card*/

.example-header{
    flex-direction: column;
    gap: 20px;
    text-align: center;
}
.example-area{
    justify-content: space-between;
    margin-block: 30px;
    flex-wrap: wrap;
}
.example-card{
    width: 23%;
    position: relative;
    height: 300px;
    background-color: black;
    background: linear-gradient(rgb(0,0,0,0.1), rgb(0,0,0,0.8)), url(../assets/asset\ 34.jpeg);
    background-size: cover;
}
.example-card:hover{
    box-shadow: 0 0 10px #888;
    transition: 0.2s ease-out;
}
.example-card:nth-child(2){
    background: linear-gradient(rgb(0,0,0,0.1), rgb(0,0,0,0.8)), url(../assets/asset\ 35.jpeg);
    background-size: cover;
}
.example-card:nth-child(3){
    background: linear-gradient(rgb(0,0,0,0.1), rgb(0,0,0,0.8)), url(../assets/asset\ 36.jpeg);
    background-size: cover;
}
.example-card:nth-child(4){
    background: linear-gradient(rgb(0,0,0,0.1), rgb(0,0,0,0.8)), url(../assets/asset\ 37.jpeg);
    background-size: cover;
}
.card-text{
    position: absolute;
    bottom: 20px;
    right: 20px;
    left: 20px;
    color: white;
}
.cta-container{
    flex-direction: column;
    gap: 30px;
    color: white;
}
.cta-container p{
    color: white;
    padding-top: 20px;
}
.cta-section{
    background-color: #183b54;
    padding: 120px var(--padding-inline-section);
}

/* footer */
footer{
    padding-block: 80px;
    background-color: #ebf2eb;
}
.footer-container{
    align-items: flex-start;
    justify-content: space-between;
}
.link-col{
    flex-direction: column;
    align-items: flex-start;
    gap: 20px;
}

/* sub footer*/

.sub-footer{
    background-color:#b9cde4;
    padding: 20px var(--padding-inline-section);
}
.subfooter-container{
    justify-content: center;
    gap:30px;
    flex-wrap: wrap;
}

</style>