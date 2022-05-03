<template>
  <footer>
    <div id="footerTexts">
      <div id="sobre">
        <h2 class="sobre">Sobre</h2>
        <p class="sobreText">Lorem Ipsum</p>
        <p>Lorem Ipsum</p>
        <p>Lorem Ipsum</p>
      </div>
      <div id="investir">
        <h2 class="investir">Investir</h2>
        <div id="investirText">
          <p class="investirText">Lorem Ipsum</p>
          <p>Lorem Ipsum</p>
          <p>Lorem Ipsum</p>
        </div>
      </div>
      <div id="aprender">
        <h2 class="aprender">Aprender</h2>
        <div id="aprenderText">
          <p class="aprenderText">Lorem Ipsum</p>
          <p>Lorem Ipsum</p>
          <p>Lorem Ipsum</p>
        </div>
      </div>
      <div id="faleConosco">
        <h2 class="faleConosco">Fale Conosco</h2>
        <div id="faleConoscoText">
          <p class="faleConoscoText">Lorem Ipsum</p>
          <p>Lorem Ipsum</p>
          <p>Lorem Ipsum</p>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "FooterPage",
}
</script>

<style scoped>
footer {
  background-color: gray;
  height: 75vh;
  display: flex;
  justify-content: center;
  align-items: flex-end;
}

#footerTexts {
  height: 70vh;
  width: 100ch;
  font-size: 20px;
  display: flex;
  justify-content: space-evenly;
}

.sobreText {
  padding-top: 20px;
}

.investirText {
  padding-top: 20px;
}

.aprenderText {
  padding-top: 20px;
}

.faleConoscoText {
  padding-top: 20px;
}
</style>
