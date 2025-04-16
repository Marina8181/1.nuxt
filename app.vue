<template>
  <div>
    <header>
      <h1>Добро пожаловать!</h1>
    </header>

    <div class="container">
      <div class="left">
        <h2>Кто я?</h2>
        <img src="/pictures/пингвин.jpg"  alt="пингвин" style="width: 100%; height: auto; border-radius: 10px;">
        <ul>
          <li>Студентка ДВФУ</li>
          <li>Любитель кошек</li>
          <li>Кофеман</li>
        </ul>
      </div>
      <div class="middle">npm run dev
        <h2>Здравствуйте))</h2>
        <p id="greeting">Hello, World</p>
        <img src="/pictures/китик.png"  alt="котенок" style="width: 500px; height: auto; border-radius: 10px; padding-right: 110px;">
        <button @click="changeGreeting">Поменять приветствие</button>
      </div>
      <div class="right">
        <h2>Что это за сайт?</h2>
        <img src="/pictures/сова.jpg" alt="сова" style="width: 100%; height: auto; border-radius: 20px;">
        <p>Это вторая домашняя работа по frontend разработке.</p>
      </div>
    </div>

    <footer>
      <p>Обратная связь: <a href="mailto:motuz.mb@dvfu.ru" style="color: black;">motuz.mb@dvfu.ru</a></p>
      <p>Автор: Мотуз Марина</p>
    </footer>
  </div>
</template>

<script>
export default {
  methods: {
    changeGreeting() {
      const greetingElement = document.getElementById('greeting');
      if (greetingElement.innerText === "Hello, World") {
        greetingElement.innerText = "Hello, FEFU";
      } else {
        greetingElement.innerText = "Hello, World";
      }
    }
  }
}
</script>

<style scoped>
:root {
  --font-family-one: 'Open Sans', sans-serif;
  --font-family-two: 'Montserrat', sans-serif;
}

body {
  margin: 0;
  font-family: var(--font-family-one);
}

header {
  background-color: lightblue;
  padding: 20px;
  margin: 10px;
  text-align: center;
}

.container {
  display: flex;
  gap: 10px;
  margin: 10px;
  height: 600px;
}

.left, .right {
  width: 400px;
  background-color: #228B22;
  padding: 20px;
}

.middle {
  width: 1000px;
  background-color: #FFF273;
  padding: 20px;
  text-align: center;
}

footer {
  background-color: teal;
  text-align: center;
  padding: 10px;
  margin: 10px;
}

button {
  margin-top: 10px;
}

header h1 {
  font-family: var(--font-family-two);
}

h2 {
  font-family: var(--font-family-two);
}
</style>
