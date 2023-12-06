<template>
    <div class="outside_container" @mouseover="showAdditionalInfo" @mouseout="hideAdditionalInfo">
      <img src="@/assets/viktoriia_photo.jpg" alt="photo">
      <div class="text_container">
        <p class="name_text">Derpak Viktoriia</p>
        <p class="position_text">Project Manager</p>
      </div>
      <div class="additional_info_container">
        <p>
          Viktoriia Derpak aka fuvaji. 
        </p>
        <p>
          Project Manager / Backend Developer / Senior Valorant Player. 
        </p>
        <p>
          nah, I'd win.
        </p>
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
    text-align: center;
    font-weight: normal;
    padding-left: 2%;
  }
  .additional_info_container {
    display: none;
    text-align: center;
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
  </style>
  