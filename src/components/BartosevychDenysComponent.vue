<template>
  <div class="outside_container" @mouseover="showAdditionalInfo" @mouseout="hideAdditionalInfo">
    <img class="denys-img" src="@/assets/denys_photo.png" alt="photo">
    <div class="text_container">
      <p class="name_text">Bartosevych Denys</p>
      <p class="position_text">Full-stack Developer</p>
    </div>
    <div class="additional_info_container">
        <div class="bartosevych_denys_description_div">
          <p>.NET C# Enjoyer</p>
          <p class="clown_emoji">🤡</p>
          <p>known as jscd</p>
        </div>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    showAdditionalInfo() {
      const additionalInfoContainer = this.$el.querySelector('.additional_info_container');
      additionalInfoContainer.style.display = 'block';
    },
    hideAdditionalInfo() {
      const additionalInfoContainer = this.$el.querySelector('.additional_info_container');
      additionalInfoContainer.style.display = 'none';
    }
  }
}
</script>

<style scoped>
.outside_container {
  height: 25%;
  width: 20%;
  background-color: #d9d9d9;
  border-radius: 50px;
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: 3%;
}

.outside_container img {
  margin: 10% 10% 0 10%;
  height: 150px;
  width: 150px;
  border-radius: 100px;
}

.name_text {
  font-family: 'Montserrat', sans-serif;
  font-size: 26px;
  font-weight: bold;
}

.position_text {
  font-family: 'Montserrat', sans-serif;
  font-size: 20px;
  font-weight: normal;
  padding-left: 2%;
  text-align: center;
}
.additional_info_container {
  display: none;
  border-radius: 50px;
}
.additional_info_container p{
  font-family: 'Montserrat', sans-serif;
  font-size: 14px;
  margin-left: 5%;
  margin-right: 5%;
  padding-bottom: 3%;
}
.outside_container:hover .additional_info_container {
  display: block;
}

.bartosevych_denys_description_div{
  flex-direction: column;
  display: flex;
  justify-content: center;
  align-items: center;
}

.bartosevych_denys_description_div p{
  width: 100%;
  text-align: center;
}

.clown_emoji:hover{
  animation: clownAnimation 1s infinite linear;
}

@keyframes clownAnimation {
  0% {
    transform: scale(100%) rotate(0);
  }
  50% {
    transform: scale(200%) rotate(180deg);
  }
  100% {
    transform: scale(100%) rotate(360deg);
  }
}
.denys-img{
  transition: transform 1s;
}

.denys-img:hover {
  animation: rotationAnimation 4s infinite linear;
}

@keyframes rotationAnimation {
  0%{
    transform: rotate(0);
  }
  100%{
    transform: rotate(360deg);
  }
}
</style>
