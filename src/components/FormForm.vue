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
          <input type="text" class="mediumInput" name="email" required />
          <input
            type="text"
            class="mediumInput paddingInput"
            name="confirmacao"
            required
          />
        </div>
        <div id="labelNumbers">
          <label>Cpf</label>
          <label>Celular</label>
        </div>
        <div id="numbers">
          <input type="number" class="mediumInput" name="cpf" required />
          <input
            type="number"
            class="mediumInput paddingInput"
            name="celular"
            required
          />
        </div>
        <label>Data de nascimento</label>
        <br />
        <input type="date" class="mediumInput data" name="data" required />
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
        <p>
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Orci,
          volutpat in <br />iaculis nec nisl tellus. Amet tellus nunc dolor
          magna risus. <br />Habitant neque, id risus diam
        </p>
        <br />
        <div id="button">
          <button class="btn next1" @click="hiddenForm1">Enviar</button>
        </div>
      </form>

      <form id="form2" hidden>
        <br />
        <div id="texts">
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
          <input type="text" class="mediumInput" required />
          <input type="text" class="mediumInput paddingInput" required />
        </div>
        <div id="labelLogradouro2">
          <label>Cep</label>
          <label>Endereço</label>
        </div>
        <div id="logradouro2">
          <input type="text" class="mediumInput" required />
          <input type="text" class="mediumInput paddingInput" required />
        </div>
        <label>Número</label>
        <br />
        <input type="text" class="bigInput" required />
        <div id="button">
          <button class="btn next2" @click="hiddenForm2">Confirmar</button>
        </div>
      </form>
      <form id="form3" hidden>
        <div class="success-checkmark">
          <div class="check-icon">
            <span class="icon-line line-tip"></span>
            <span class="icon-line line-long"></span>
            <div class="icon-circle"></div>
            <div class="icon-fix"></div>
          </div>
        </div>
        <br />
        <div id="title">
          <h1 class="title3">
            Cadastro <br />
            Finalizado
          </h1>
        </div>
        <br />
        <div id="text">
          <p class="text3">
            Caso deseja retornar à página inicial <br />
            no botão a baixo
          </p>
          <br />
        </div>
        <div id="button">
          <button class="btn2 next2">Continuar</button>
        </div>
      </form>
    </div>
  </div>
</template>

<script>
export default {
  name: "FormForm",
  methods: {
    hiddenForm1() {
      document.getElementById("form1").style = "display: none;";
      document.getElementById("form3").style = "display: none;";
      document.getElementById("form2").style = "display: block;";
    },
    hiddenForm2() {
      document.getElementById("form2").style = "display: none;";
      document.getElementById("form3").style = "display: block;";
    },
  },
};
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
  justify-content: center;
}

#form1 {
  z-index: 0;
  right: -450;
}

#form2 {
  position: absolute;
  z-index: 2;
}

#form3 {
  position: absolute;
  left: 30%;
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

.title3 {
  text-align: center;
}

.text3 {
  text-align: center;
}

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

.btn2 {
  font-size: 20px;
  padding: 10px 55px;
  border: 0px;
  border-radius: 30px;
  color: white;
  background-color: gray;
  cursor: pointer;
  align-items: center;
}

.btn:hover {
  background-color: rgba(255, 20, 106, 0.616);
}

.btn2:hover {
  background-color: rgba(128, 128, 128, 0.616);
}

#form2 {
  left: 450px;
}

.success-checkmark {
  width: 80px;
  height: 115px;
  margin: 0 auto;
}
.success-checkmark .check-icon {
  width: 80px;
  height: 80px;
  position: relative;
  border-radius: 50%;
  box-sizing: content-box;
  border: 4px solid #4caf50;
}
.success-checkmark .check-icon::before {
  top: 3px;
  left: -2px;
  width: 30px;
  transform-origin: 100% 50%;
  border-radius: 100px 0 0 100px;
}
.success-checkmark .check-icon::after {
  top: 0;
  left: 30px;
  width: 60px;
  transform-origin: 0 50%;
  border-radius: 0 100px 100px 0;
  animation: rotate-circle 4.25s ease-in;
}
.success-checkmark .check-icon::before,
.success-checkmark .check-icon::after {
  content: "";
  height: 100px;
  position: absolute;
  background: #ffffff;
  transform: rotate(-45deg);
}
.success-checkmark .check-icon .icon-line {
  height: 5px;
  background-color: #4caf50;
  display: block;
  border-radius: 2px;
  position: absolute;
  z-index: 10;
}
.success-checkmark .check-icon .icon-line.line-tip {
  top: 46px;
  left: 14px;
  width: 25px;
  transform: rotate(45deg);
  animation: icon-line-tip 0.75s;
}
.success-checkmark .check-icon .icon-line.line-long {
  top: 38px;
  right: 8px;
  width: 47px;
  transform: rotate(-45deg);
  animation: icon-line-long 0.75s;
}
.success-checkmark .check-icon .icon-circle {
  top: -4px;
  left: -4px;
  z-index: 10;
  width: 80px;
  height: 80px;
  border-radius: 50%;
  position: absolute;
  box-sizing: content-box;
  border: 4px solid rgba(76, 175, 80, 0.5);
}
.success-checkmark .check-icon .icon-fix {
  top: 8px;
  width: 5px;
  left: 26px;
  z-index: 1;
  height: 85px;
  position: absolute;
  transform: rotate(-45deg);
  background-color: #ffffff;
}

@keyframes rotate-circle {
  0% {
    transform: rotate(-45deg);
  }
  5% {
    transform: rotate(-45deg);
  }
  12% {
    transform: rotate(-405deg);
  }
  100% {
    transform: rotate(-405deg);
  }
}
@keyframes icon-line-tip {
  0% {
    width: 0;
    left: 1px;
    top: 19px;
  }
  54% {
    width: 0;
    left: 1px;
    top: 19px;
  }
  70% {
    width: 50px;
    left: -8px;
    top: 37px;
  }
  84% {
    width: 17px;
    left: 21px;
    top: 48px;
  }
  100% {
    width: 25px;
    left: 14px;
    top: 45px;
  }
}
@keyframes icon-line-long {
  0% {
    width: 0;
    right: 46px;
    top: 54px;
  }
  65% {
    width: 0;
    right: 46px;
    top: 54px;
  }
  84% {
    width: 55px;
    right: 0px;
    top: 35px;
  }
  100% {
    width: 47px;
    right: 8px;
    top: 38px;
  }
}
</style>
