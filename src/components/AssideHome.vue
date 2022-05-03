<template>
  <aside>
    <div id="divAside">
      <div id="asidTexts">
        <div id="asideTitle">
          <h2 class="asideTitle">Investir é sobre você</h2>
        </div>
        <div id="asideText">
          <p class="asideText">
            COMEÇE A INVESTIR EM POUCOS MINUTOS. DESCOMPLIQUE.
          </p>
        </div>
      </div>
      <div id="asideButton">
        <input type="button" value="Button" class="asideButton" />
      </div>
    </div>
  </aside>
</template>

<script>
export default {
  name: "AssidePage",
}
</script>

<style scoped>
#divAside {
  background-color: rgb(203, 198, 198);
  height: 25vh;
  display: flex;
  justify-content: space-around;
  align-items: center;
}

.asideTitle {
  font-size: 40px;
}

.asideText {
  font-size: 20px;
}

#asideButton {
  display: flex;
}

.asideButton {
  font-size: 20px;
  padding: 10px 55px;
  border: 0px;
  border-radius: 30px;
  color: white;
  background-color: black;
}

.asideButton:hover {
  background-color: rgba(0, 0, 0, 0.616);
}
</style>
