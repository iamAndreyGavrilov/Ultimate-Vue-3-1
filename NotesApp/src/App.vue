<template>
  <main>
    <div class="container">
      <header>
        <h1>Notes</h1>
        <button>+</button>
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

<script setup>

</script>

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

button {
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
</style>