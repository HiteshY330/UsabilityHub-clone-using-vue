<template>
  <div id="app">
    <Useability/>
  </div>
</template>

<script>
import Useability from './components/UseabilityWeb.vue';

export default {
  name: 'App',
  components: {
    Useability
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;500&family=Roboto:wght@400;700&display=swap');

*{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
:root{
    --primary-text-color:#183b56;
    --secondary-text-color:#577592;
    --accent-color:#2294ed;
    --accent-color-dark:#1d69a3;
    --padding-inline-section:20px; 
}
body{
    font-family: 'poppins', sans-serif;
    color: var(--primary-text-color);
}
h1{
    font-size: 3rem;
}
h2{
    font-size: 2rem;
}
h3{
    font-size: 1.5rem;
}
p{
    font-family: 'Roboto',sans-serif;
    font-size: 1.25rem;
    color: var(--secondary-text-color);
    line-height: 1.8rem;
}
a{
    text-decoration: none;
    display: inline-block;
}
.flex{
    display: flex;
    align-items: center;
}
ul{
    list-style: none;
}
.small-bold-text{
    font-size: 1rem;
    font-weight:  700;
}
.container{
    max-width: 1180px;
    margin-inline: auto;
    padding-inline: var(--padding-inline-section);
    overflow: hidden;
}
.primary-button{
    background-color:var(--accent-color);
    border-radius:6px;
    font-weight:700;
    color:white !important;
    padding:12px 24px;
    box-shadow:0 0 2px var(--secondary-text-color);
    transition: 0.2s ease-out;
    text-align: center;
}
.primary-button:hover{
    background-color: var(--accent-color-dark);
}
.secondary-button{
    border: 0.5px solid var(--secondary-text-color);
    border-radius: 6px;
    font-weight:700;
    color: var(--primary-text-color) !important;
    padding:12px 24px;
    box-shadow:0 0 2px var(--secondary-text-color);
    transition: 0.2s ease-out;
}
.secondary-button:hover{
    border-color:var(--accent-color);
    color: var(--accent-color) !important;
}
@media screen and (max-width:991px) {
    h3{
        font-size: 1.2rem;
    }
    .nav-toggle{
        display: block;
        margin-right: 20px;
    }
    .main-nav{
        position: relative;
        overflow: initial;
    }
    .nav-links{
        /*display: none;*/
        position: absolute;
        background-color: white;
        top: 100%;
        left: -100%;
        width: 100%;
        transition: 0.3s ease-out;
    }
    .nav-links.active{
        left: 0;
    }
    .nav-links ul{
        flex-direction: column;
        margin-block: 40px;
    }
    .big-feature-container:nth-child(2){
        flex-direction: row-reverse;
    }
    .example-area{
        gap: 20px;
    }
    .example-card{
        width:calc(50% - 10px);
        height: 180px;
    }
    .cta-section{
        padding-block: 50px;
    }
}

@media screen and (max-width:676px) {
    .primary-button{
        width: 100%;
    }
    .header-section{
        flex-direction: column-reverse;
    }
    .left-header{
        max-width: 100vw;
        text-align: center;
    }
    .features-card{
        min-width: calc(50% - 20px);
    }
    .big-feature-container{
        flex-direction: column;
        text-align: center;
        margin-block: 20px;
    }
    .big-feature-container:nth-child(2){
        flex-direction: column;
    }
    .footer-container{
        flex-direction: column;
        text-align: center;
        align-items: center;
        gap: 40px;
    }
    .link-col{
        align-items: stretch;
    }
}

@media screen and (max-width:479px) {
    :root{
        --padding-inline-section:10px; 
    }
    h1{
        font-size: 2rem;
    }
    h2{
        font-size: 1rem;
    }
    p{
        font-size: 1rem;
    }
    .features-card{
        min-width: 100%;
    }
    .example-card{
        width: 100%;
    }
    .cta-container {
        text-align: center;
    }
}

</style>
