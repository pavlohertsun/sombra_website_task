<template>
  <div class="main_container">
    <div class="text_container">
      Welcome to Sigma Software website
      <br>Read more about our
      <a href="#" @click="scrollToDiv">team</a>
    </div>
  </div>
  <div class="target_div">
    <h2 class="text_styles">
      Our team
    </h2>
    <div class="team_container">
      <pavlo-hertsun-component></pavlo-hertsun-component>
      <derpak-viktoriia-component></derpak-viktoriia-component>
    </div>
    <div class="team_container">
      <hladun-victor-component></hladun-victor-component>

      <bartosevych-denys-component></bartosevych-denys-component>
    </div>

  </div>
</template>

<script>
import PavloHertsunComponent from "@/components/PavloHertsunComponent.vue";
import DerpakViktoriiaComponent from "./components/DerpakViktoriiaComponent.vue";
import BartosevychDenysComponent from "@/components/BartosevychDenysComponent.vue";
import HladunVictorComponent from "@/components/HladunVictorComponent.vue";

export default {
  components: {HladunVictorComponent,BartosevychDenysComponent , PavloHertsunComponent, DerpakViktoriiaComponent},
  methods: {
    scrollToDiv() {
      const targetDiv = document.querySelector('.target_div');
      targetDiv.scrollIntoView({ behavior: 'smooth' });
    }
  }
}

</script>

<style scoped>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.main_container {
  height: 1080px;
  width: 1920px;
  text-align: center;
  background: url('@/assets/homepageimage1.png') no-repeat;
  background-size: cover;
  background-position: center;
}

.text_container {
  font-family: 'Montserrat', sans-serif;
  font-size: 32px;
  font-weight: 400;
  color: #d9d9d9;
  text-align: right;
  padding-top: 15%;
  padding-right: 25%;
}

.target_div {
  height: 500px;
  width: 100%;
  background-color: #282828;
}
.target_div h2{
  text-align: center;
}
.text_styles{
  font-family: 'Montserrat', sans-serif;
  font-size: 32px;
  font-weight: 400;
  color: #d9d9d9;
}
.team_container{
  display: flex;
  flex-direction: row;
  justify-content: center;

}
</style>
