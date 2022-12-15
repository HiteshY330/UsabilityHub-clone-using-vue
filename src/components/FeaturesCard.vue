<template>
  <div class="features-section">
    <div class="container">
      <div class="features-header">
        <h2>Your user research Swiss Army knife</h2>
        <a href="#" class="secondary-button"
          >See all features <i class="fa-solid fa-arrow-right"> </i
        ></a>
      </div>
      <div class="features-area flex">
        <div class="features-card flex" v-for="(card, i) in features" :key="i">
          <img :src="card.img" alt="features" />
          <h3>{{ card.heading }}</h3>
          <p>{{ card.ptag }}</p>
          <a href="#" class="secondary-button"
            >{{ card.learmore }}<i class="fa-solid fa-arrow-right"> </i
          ></a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import image from "../assets/asset 11.svg";
import image1 from "../assets/asset 13.svg";
import image2 from "../assets/asset 14.svg";
import image3 from "../assets/asset 15.svg";
import image4 from "../assets/asset 16.svg";
import image5 from "../assets/asset 17.svg";

export default {
  data() {
    return {
      features: [
        {
          name: "Card sorting",
          img: image,
          heading: "Card sorting",
          ptag: "Discover how people group and label information.",
          learmore: "Learn more  ",
        },
        {
          name: "Card sorting",
          img: image1,
          heading: "Card sorting",
          ptag: "Discover how people group and label information.",
          learmore: "Learn more  ",
        },
        {
          name: "Card sorting",
          img: image2,
          heading: "Card sorting",
          ptag: "Discover how people group and label information.",
          learmore: "Learn more  ",
        },
        {
          name: "Card sorting",
          img: image3,
          heading: "Card sorting",
          ptag: "Discover how people group and label information.",
          learmore: "Learn more  ",
        },
        {
          name: "Card sorting",
          img: image4,
          heading: "Card sorting",
          ptag: "Discover how people group and label information.",
          learmore: "Learn more  ",
        },
        {
          name: "Card sorting",
          img: image5,
          heading: "Card sorting",
          ptag: "Discover how people group and label information.",
          learmore: "Learn more  ",
        },
      ],
    };
  },
};
</script>

<style>
.features-section {
  padding: 60px var(--padding-inline-section) 0;
  background-image: url(../assets/asset32.svg);
  background-repeat: no-repeat;
  background-position: center;
}
.features-header,
.example-header {
  text-align: center;
  margin-bottom: 20px;
}
.features-header h2,
.example-header h2 {
  margin-bottom: 20px;
}
.features-area {
  flex-wrap: wrap;
  justify-content: space-between;
  gap: 20px;
  margin-top: 40px;
}
.features-card {
  flex-direction: column;
  gap: 20px;
  max-width: 30%;
  text-align: center;
}
</style>