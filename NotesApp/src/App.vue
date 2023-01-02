<script setup>
import {ref} from 'vue'

const showModal = ref(false)

</script>

<template>
  <main>
    <div v-show="showModal" class="overlay">
      <div class="modal">
        <textarea name="note" id="note" cols="30" rows="10"></textarea>
        <button>Add Note</button>
        <button class="close" @click="showModal = false">Close</button>
      </div>
    </div>
    <div class="container">
      <header>
        <h1>Notes</h1>
        <button class="btn" @click="showModal = true">+</button>
      </header>
      <div class="cards-container">
        <div class="card">
          <p class="main-text">Lorem ipsum dolor sit amet, consectetur adipisicing elit. At atque dolores id neque
            quaerat vero.</p>
          <p class="date">02/01/2023</p>
        </div>
        <div class="card">
          <p class="main-text">Lorem ipsum dolor sit amet, consectetur adipisicing elit. At atque dolores id neque
            quaerat vero.</p>
          <p class="date">02/01/2023</p>
        </div>
      </div>
    </div>
  </main>
</template>


<style scoped>
main {
  height: 100vh;
  width: 100vw;
}

.container {
  max-width: 1000px;
  margin: 0 auto;
  padding: 10px;
}

header {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

h1 {
  font-size: 75px;
  font-weight: bold;
  /*margin-bottom: 25px;*/
}

.btn {
  cursor: pointer;
  border: none;
  padding: 10px;
  width: 50px;
  height: 50px;
  border-radius: 50%;
  background-color: #000000;
  color: #ffffff;
  font-size: 30px;
  font-weight: bold;
}

.card {
  width: 225px;
  height: 225px;
  background-color: rgb(213, 182, 46);
  border-radius: 10px;
  margin: 10px;
  padding: 10px;
  box-shadow: 0 0 15px 0 rgba(0, 0, 0, 1);
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

.main-text {
  font-size: 20px;
}

.date {
  font-size: 15px;
  font-weight: bold;
}

.cards-container {
  display: flex;
  flex-wrap: wrap;
}

.overlay {
  position: absolute;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.5);
  z-index: 1;
  display: flex;
  justify-content: center;
  align-items: center;
}

.modal {
  position: relative;
  width: 750px;
  background-color: #ffffff;
  border-radius: 10px;
  padding: 30px;
  display: flex;
  flex-direction: column;
}

textarea {
  width: 100%;
  height: 100%;
  resize: none;
  font-size: 20px;
}

.modal button {
  padding: 10px 20px;
  font-size: 20px;
  width: 100%;
  border: none;
  border-radius: 10px;
  background-color: #000000;
  color: white;
  cursor: pointer;
  margin-top: 20px;
}

.modal .close {
  background-color: red;
}
</style>