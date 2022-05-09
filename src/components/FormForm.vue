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
        <input
          type="text"
          class="bigInput name"
          name="nome"
          autocomplete="off"
        />
        <div id="labelEmail">
          <label>E-mail</label>
          <label>Confirmar e-mail</label>
        </div>
        <div id="email">
          <input
            type="text"
            class="mediumInput email"
            name="email"
            autocomplete="off"
          />
          <input
            type="text"
            class="mediumInput paddingInput confirmacao"
            name="confirmacao"
            formtarget="email"
            autocomplete="off"
          />
        </div>
        <div id="labelNumbers">
          <label>Cpf</label>
          <label>Celular</label>
        </div>
        <div id="numbers">
          <input
            type="text"
            class="mediumInput cpf"
            name="cpf"
            maxlength="14"
            autocomplete="off"
            pattern="[0-9]{11}"
            onblur="formataCPF(this)"
          />
          <input
            type="text"
            class="mediumInput paddingInput celphone"
            name="celular"
            min="1"
            onblur="mascaraDeTelefone(this)"
            onfocus="tiraHifen(this)"
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
        <p>
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Orci,
          volutpat in <br />iaculis nec nisl tellus. Amet tellus nunc dolor
          magna risus. <br />Habitant neque, id risus diam
        </p>
        <br />
        <div id="button">
          <input
            type="button"
            class="btn next1"
            value="confirmar"
            @click="hiddenForm1"
          />
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
          <input type="text" class="mediumInput contry" required />
          <input type="text" class="mediumInput paddingInput city" required />
        </div>
        <div id="labelLogradouro2">
          <label>Cep</label>
          <label>Endereço</label>
        </div>
        <div id="logradouro2">
          <input type="number" class="mediumInput cep" required />
          <input
            type="text"
            class="mediumInput paddingInput address"
            required
          />
        </div>
        <label>Número</label>
        <br />
        <input type="number" class="bigInput number" required />
        <div id="button">
          <input
            type="button"
            class="btn next2"
            value="Confirmar"
            @click="hiddenForm2()"
          />
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
        <div id="button3">
          <a href="/" class="btn2">Continuar</a>
        </div>
      </form>
    </div>
  </div>
</template>

<script>
export default {
  name: "FormForm",
  methods: {
    cpfMask() {
      function formataCPF(cpf) {
        const elementoAlvo = cpf;
        const cpfAtual = cpf.value;

        let cpfAtualizado;

        cpfAtualizado = cpfAtual.replace(
          /(\d{3})(\d{3})(\d{3})(\d{2})/,
          function (regex, argumento1, argumento2, argumento3, argumento4) {
            return (
              argumento1 +
              "." +
              argumento2 +
              "." +
              argumento3 +
              "-" +
              argumento4
            );
          }
        );
        elementoAlvo.value = cpfAtualizado;
      }

      const cpf = document.querySelector("cpf");
      cpf.addEventListener("input", function (event) {
        if (cpf.validity.patternMismatch) {
          cpf.setCustomValidity("Deveria ter apenas números aqui =) ");
          btnEnviar.disabled = true;
        } else {
          cpf.setCustomValidity("");
          btnEnviar.disabled = false;
        }
      });
    },

    // telphoneMask() {
    //   function mascaraDeTelefone(telefone) {
    //     const textoAtual = telefone.value;
    //     const isCelular = textoAtual.length === 9;

    //     let textoAjustado;
    //     if (isCelular) {
    //       const parte1 = textoAtual.slice(0, 5);
    //       const parte2 = textoAtual.slice(5, 9);
    //       textoAjustado = `${parte1}-${parte2}`;
    //     } else {
    //       const parte1 = textoAtual.slice(0, 4);
    //       const parte2 = textoAtual.slice(4, 8);
    //       textoAjustado = `${parte1}-${parte2}`;
    //     }

    //     telefone.value = textoAjustado;
    //   }

    //   function tiraHifen(telefone) {
    //     const textoAtual = telefone.value;
    //     const textoAjustado = textoAtual.replace(/\-/g, "");

    //     telefone.value = textoAjustado;
    //   }
    // },

    hiddenForm1() {
      const Nome = document.querySelector(".name").value;
      const Email = document.querySelector(".email").value;
      const Confirmacao = document.querySelector(".confirmacao").value;
      const CPF = document.querySelector(".cpf").value;
      const Celular = document.querySelector(".celphone").value;

      function isCPF(strCPF) {
        var Soma;
        var Resto;
        var i;
        Soma = 0;
        if (strCPF == "00000000000") return false;

        for (i = 1; i <= 9; i++)
          Soma = Soma + parseInt(strCPF.substring(i - 1, i)) * (11 - i);
        Resto = (Soma * 10) % 11;

        if (Resto == 10 || Resto == 11) Resto = 0;
        if (Resto != parseInt(strCPF.substring(9, 10))) return false;

        Soma = 0;
        for (i = 1; i <= 10; i++)
          Soma = Soma + parseInt(strCPF.substring(i - 1, i)) * (12 - i);
        Resto = (Soma * 10) % 11;

        if (Resto == 10 || Resto == 11) Resto = 0;
        if (Resto != parseInt(strCPF.substring(10, 11))) return false;
        return true;
      }
      var strCPF = CPF;

      function isEmail() {
        var reg = /^\w+([-+.']\w+)*@\w+([-.]\w+)*\.\w+([-.]\w+)*$/;

        if (reg.test(Email)) {
          return true;
        } else {
          return false;
        }
      }

      function sameEmail() {
        if (Email === Confirmacao && Email !== "") {
          return true;
        } else {
          return false;
        }
      }

      function isWritten() {
        if (
          Nome !== "" ||
          Email !== "" ||
          Confirmacao !== "" ||
          CPF !== "" ||
          Celular !== ""
        ) {
          return true;
        } else {
          return false;
        }
      }

      function confirmation() {
        if (
          isCPF(strCPF) === true &&
          isEmail() === true &&
          sameEmail() === true &&
          isWritten() === true
        ) {
          return true;
        } else {
          return false;
        }
      }

      if (confirmation() === true) {
        document.getElementById("form1").style = "display: none;";
        document.getElementById("form2").style = "display: block;";
        document.getElementById("form3").style = "display: none;";
      } else {
        alert("Preencha todos os campos corretamente");
      }
    },
    hiddenForm2() {
      var Pais = document.querySelector(".contry").value;
      var Cidade = document.querySelector(".city").value;
      var CEP = document.querySelector(".cep").value;
      var Endereco = document.querySelector(".address").value;
      var Number = document.querySelector(".number").value;

      function rte() {
        if (
          (Pais !== "") |
          (Cidade !== "") |
          (CEP !== "") |
          (Endereco !== "") |
          (Number !== "")
        ) {
          return true;
        } else {
          return false;
        }
      }

      if (rte() === true) {
        document.getElementById("form2").style = "display: none;";
        document.getElementById("form1").style = "display: none;";
        document.getElementById("form3").style = "display: block;";
      } else {
        alert("Preencha todos os campos corretamente");
      }
    },
  },
};
</script>

<style scoped>
* {
  color: rgb(0, 0, 0);
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
}

#button3 {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.btn:hover {
  background-color: rgba(255, 20, 106, 0.616);
}

.btn2:hover {
  background-color: rgba(128, 128, 128, 0.616);
}

.bottonText {
  font: bold;
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
