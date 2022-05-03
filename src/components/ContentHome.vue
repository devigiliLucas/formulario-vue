<template>
  <div id="divMain">
    <div id="mainContents1">
      <div id="mainPhoto1">
        <img
          src="../assets/PESSOAS_06.jpg"
          alt="Foto de um homem olhando para a camera"
          id="mainPhoto1"
        />
      </div>
      <div id="mainText1">
        <h2 id="mainTitle1">Loren Ipsum</h2>
        <p class="mainText1">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsam
          veritatis aut consequuntur iste dolore pariatur, quia, perferendis
          doloremque illo quaerat voluptas. Sunt perspiciatis facilis error
          dolor veritatis unde nulla magni.
        </p>
        <div id="mainButton1">
          <input type="button" value="Button" class="mainButton1" />
        </div>
      </div>
    </div>
    <div id="mainContents2">
      <div id="mainPhoto2">
        <img
          src="../assets/PESSOAS_11.jpg"
          alt="Foto de aerea uma rodovia"
          id="mainPhoto2"
        />
      </div>
      <div id="mainText2">
        <h2 id="mainTitle2">Loren Ipsum</h2>
        <p class="mainText2">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsam
          veritatis aut consequuntur iste dolore pariatur, quia, perferendis
          doloremque illo quaerat voluptas. Sunt perspiciatis facilis error
          dolor veritatis unde nulla magni.
        </p>
        <div id="mainButton2">
          <input type="button" value="Button" class="mainButton2" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>

export default {
  name: "ContentPage",
}
</script>

<style scoped>
#divMain {
  height: 100vh;
}

#mainContents1 {
  height: 50vh;
  display: flex;
  align-items: center;
}

#mainPhoto1 {
  width: 60%;
  height: auto;
  display: flex;
  justify-content: center;
}

#mainText1 {
  height: 50vh;
  width: 50%;
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
}

#mainTitle1 {
  font-size: 40px;
  color: black;
}

.mainText1 {
  width: 75%;
  font-size: 20px;
  color: black;
}

.mainButton1 {
  font-size: 20px;
  padding: 10px 55px;
  border: 0px;
  border-radius: 30px;
  color: white;
  background-color: rgb(255, 20, 106);
}

.mainButton1:hover {
  background-color: rgba(255, 20, 106, 0.616);
}

#mainContents2 {
  height: 50vh;
  display: flex;
  flex-direction: row-reverse;
  align-items: center;
}

#mainPhoto2 {
  width: 60%;
  height: auto;
  display: flex;
  justify-content: center;
}

#mainText2 {
  height: 50vh;
  width: 50%;
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
  align-items: flex-end;
  text-align: end;
}

#mainTitle2 {
  font-size: 40px;
  color: black;
}

.mainText2 {
  width: 75%;
  font-size: 20px;
  color: black;
}

.mainButton2 {
  font-size: 20px;
  padding: 10px 55px;
  border: 0px;
  border-radius: 30px;
  color: white;
  background-color: rgb(255, 20, 106);
}

.mainButton2:hover {
  background-color: rgba(255, 20, 106, 0.616);
}
</style>
