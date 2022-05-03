<template>
  <div id="divBanner">
    <div id="bannerText">
      <h1>Lorem ipsum dolor sit, amet consectetur adipisicing elit.</h1>
    </div>
    <div id="bannerSubText">
      <p>Consequant leo, nec, sit sociis tellus ut amet</p>
    </div>
    <div id="bannerButton">
      <input type="button" value="Button" class="bannerButton" />
    </div>
  </div>
</template>

<script>
export default {
  name: "BannerPage",
};
</script>

<style scoped>
#divBanner {
  height: 85vh;
  background-color: grey;
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
  align-items: center;
}

#bannerText {
  width: 50%;
  font-size: 50px;
}

#bannerSubText {
  width: 50%;
  font-size: 20px;
}

#bannerButton {
  width: 50%;
}

.bannerButton {
  font-size: 20px;
  padding: 10px 55px;
  border: 0px;
  border-radius: 30px;
  color: white;
  background-color: black;
}

.bannerButton:hover {
  background-color: rgba(0, 0, 0, 0.616);
}
</style>
