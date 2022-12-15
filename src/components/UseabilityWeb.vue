<template>
<div>
  <Banner/>
  <NavBar/>
  <Header/>
  <Companies/>
  <Feature/>
  <Bigfeature/>
</div>
</template>

<script>
import Banner from './BannerTop.vue';
import NavBar from './NavBar.vue';
import Header from './HeaderHero.vue';
import Companies from './CompaniesLogo.vue';
import Feature from './FeaturesCard.vue';
import Bigfeature from './BigFeatures.vue';

export default {
    components:{
        Banner,
        NavBar,
        Header,
        Companies,
        Feature,
        Bigfeature
    }

}
</script>

<style>

</style>