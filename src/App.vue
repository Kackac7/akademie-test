<template>
  <div id="app">

    <h1>Dad Jokes</h1>

    <!--
      Toto je HTML šablona pro jeden vtip.
      Pro vtip ale chceme mít samostatnou komponentu nazvanou Joke.
      Vytvoř komponentu, vezmi HTML zakomentované níže a vlož ho
      dovnitř template komponenty.

      Do komponenty posílej potřebné props a jejich hodnoty zobrazuj
      místo textu vtipů a počtů lajků, které jsou teď v šabloně
      zadané natvrdo. Nezapomeň i na ikonku uživatele.

      Zde uvnitř App vue pak procházej pole vtipů pomocí v-for
      a zobrazuj komponentu Joke pro každý vtip na seznamu.

      Zařiď, aby tlačítka v komponentě fungovala a emitovala sem
      do App.vue události, které zde budou spouštět příslušné metody,
      které změní počty lajků u vtipu v poli.
    -->
    <!--
    <div class="joke">
      <div class="joke-body">
        <img class="joke-user" src="/images/users/user01.png" />
        <p class="joke-text">
          The secret service isn't allowed to yell "Get down!" anymore when the president is about to be attacked. Now they have to yell "Donald, duck!"
        </p>
      </div>
      <div class="joke-likes">
        <button class="btn-like btn-up"></button>
        <span class="likes-count likes-up">0</span>

        <button class="btn-like btn-down"></button>
        <span class="likes-count likes-down">0</span>
      </div>
    </div>
    -->

  </div>
</template>


<script>
export default {

}
</script>



<style>
html {
  box-sizing: border-box;
}

*, ::before, ::after {
  box-sizing: inherit;
}

body {
  font-family: sans-serif;
}

h1 {
  text-align: center;
}

.joke {
  max-width: 40rem;
  margin: 2rem auto;
}

.joke-body {
  display: flex;
}

.joke-user {
  flex: 0 0 auto;
  width: 5rem;
  height: 5rem;
  margin-right: 1rem;
}

.joke-text {
  background-color: cornflowerblue;
  color: white;
  border-radius: 1rem;
  padding: 1.5rem 2rem;
  margin: 0;
  line-height: 150%;
}

.joke-likes {
  display: flex;
  justify-content: flex-end;
  align-items: center;
  margin-top: 1rem;
}

.likes-count {
  font-size: 1.5rem;
  font-weight: bold;
  margin: 0 0.5rem;
}

.likes-up {
  color: #00e268;
}

.likes-down {
  color: #ff5654;
}

.btn-like {
  border: none;
  outline: none;
  width: 2rem;
  height: 2rem;
  border-radius: 1rem;
  background-size: 1.2rem;
  background-position: center;
  background-repeat: no-repeat;
  cursor: pointer;
  transition: transform 0.3s;
}

.btn-like:hover {
  transform: scale(1.2);
}

.btn-up {
  background-color: #00e268;
  background-image: url('/images/like-up.png');
}

.btn-down {
  background-color: #ff5654;
  background-image: url('/images/like-down.png');
}

</style>
