<template>
  <div id="contents">
    <div id="photo">
      <img
        src="../assets/Fernanda.jpg"
        alt="Mulhr com um celular"
        class="photo"
      />
    </div>
    <div id="centralBox">
      <form id="form1">
        <br />
        <div id="texts">
          <h1 class="title">Seja bem-vindo</h1>
          <br />
          <h2 class="subtitle">Dados de contato</h2>
          <br />
          <p class="text">
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Orci,
            volutpat in <br />iaculis nec nisl tellus.
          </p>
          <br />
        </div>
        <label>Nome completo</label>
        <br />
        <input type="text" class="bigInput" name="nome" required />
        <div id="labelEmail">
          <label>E-mail</label>
          <label>Confirmar e-mail</label>
        </div>
        <div id="email">
          <input type="text" class="mediumInput" name="email" />
          <input
            type="text"
            class="mediumInput paddingInput"
            name="confirmacao"
          />
        </div>
        <div id="labelNumbers">
          <label>Cpf</label>
          <label>Celular</label>
        </div>
        <div id="numbers">
          <input type="number" class="mediumInput" name="cpf" />
          <input
            type="number"
            class="mediumInput paddingInput"
            name="celular"
          />
        </div>
        <label>Data de nascimento</label>
        <br />
        <input type="date" class="mediumInput data" name="data" />
        <p class="bottonText">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit
        </p>
        <br />
        <p class="bottonText">Mattis semper odio preretium vestibulum nulla</p>
        <br />
        <div id="sms">
          <input type="checkbox" name="sms" />
          <label>Email e SMS</label>
        </div>
        <div id="mensageApp">
          <input type="checkbox" name="whatsapp" />
          <label>Whatsapp</label>
        </div>
      </form>
      <p>
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Orci, volutpat
        in <br />iaculis nec nisl tellus. Amet tellus nunc dolor magna risus.
        <br />Habitant neque, id risus diam
      </p>
      <br />
      <div id="button">
        <button class="btn next1">Continuar</button>
      </div>

      <form id="form2" hidden>
        <br />
        <div id="texts">
          hidden
          <h2 class="subtitle">Dados pessoais</h2>
          <br />
          <p class="text">
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Orci,
            volutpat in <br />iaculis nec nisl tellus.
          </p>
          <br />
        </div>
        <br />
        <div id="labelLogradouro1">
          <label>País onde reside</label>
          <label>Cidade</label>
        </div>
        <div id="logradouro1">
          <input type="text" class="mediumInput" />
          <input type="text" class="mediumInput paddingInput" />
        </div>
        <div id="labelLogradouro2">
          <label>Cep</label>
          <label>Endereço</label>
        </div>
        <div id="logradouro2">
          <input type="text" class="mediumInput" />
          <input type="text" class="mediumInput paddingInput" />
        </div>
        <label>Número</label>
        <br />
        <input type="text" class="bigInput" />
        <div id="button">
          <button class="btn next2">Continuar</button>
        </div>
      </form>
    </div>
  </div>
</template>

<script>
export default { 
  name: "FormForm",
}

</script>

<style scoped>
* {
  color: black;
}

input[type="number"]::-webkit-inner-spin-button {
  -webkit-appearance: none;
}
input[type="number"] {
  -moz-appearance: textfield;
  appearance: textfield;
}

.photo {
  height: 95vh;
  width: auto;
  position: absolute;
  right: 0px;
  top: 48px;
}

#contents {
  display: flex;
  justify-content: center;
  align-items: center;
}

#centralBox {
  height: 800px;
  width: 1100px;
  display: flex;
  flex-direction: column;
}

#form1 {
  z-index: 0;
  right: -450;
}

#form2 {
  position: absolute;
  z-index: 2;
}

input {
  margin-bottom: 20px;
  margin-top: 0px;
  border: solid 1px black;
}

/* .title {
  font-size: 50px;
}

.subtitle {
  font-size: 30px;
}

p {
  font-size: 20px;
} */

.bigInput {
  height: 50px;
  width: 528px;
  border-radius: 5px;
  font-size: 20px;
}

.mediumInput {
  height: 50px;
  width: 230px;
  border-radius: 5px;
  font-size: 20px;
}

#labelEmail {
  display: flex;
  justify-content: space-between;
  width: 410px;
}

#labelLogradouro1 {
  display: flex;
  justify-content: space-between;
  width: 340px;
}

#email {
  display: flex;
  justify-content: flex-start;
}

#logradouro1 {
  display: flex;
  justify-content: flex-start;
}

#labelNumbers {
  display: flex;
  justify-content: space-between;
  width: 340px;
}

#labelLogradouro2 {
  display: flex;
  justify-content: space-between;
  width: 355px;
}

#numbers {
  display: flex;
  justify-content: flex-start;
}

#logradouro2 {
  display: flex;
  justify-content: flex-start;
}

.paddingInput {
  margin-left: 56px;
}

.data {
  display: flex;
  flex-direction: row-reverse;
  font-weight: lighter;
}

#sms {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  width: 120px;
}

#mensageApp {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  width: 100px;
}

.btn {
  font-size: 20px;
  padding: 10px 55px;
  border: 0px;
  border-radius: 30px;
  color: white;
  background-color: rgb(255, 20, 106);
  cursor: pointer;
}

.btn:hover {
  background-color: rgba(255, 20, 106, 0.616);
}

#form2 {
  left: 450px;
}
</style>

