<template>
  <div id="app">

    <h1>Dad Jokes</h1>

   <joke 
    v-for="joke in jokes"
   v-bind:key="joke.id"
   v-bind:id="joke.id"
   v-bind:vtip="joke.vtip"
   v-bind:user="joke.user"
   v-bind:like="joke.like"
   v-bind:dislike="joke.dislike"
   v-bind:give-like="dajLike($event)"
   v-bind:give-dislike="dajDislike($event)"
/>
  </div>
</template>


<script>
import Joke from "./components/Joke.vue";

export default {
  components: {
    joke : Joke
  },
  data() {
    return {
      jokes: [
      { id: '1', vtip: 'The secret service is not allowed to yell "Get down!" anymore when the president is about to be attacked. Now they have to yell "Donald, duck!"', user: 'user01', like: '13', dislike: '24' },
    { id: '2', vtip: 'Why did the invisible man turn down the job offer? He could not see himself doing it.', user: 'user02', like: '50', dislike: '10' },
    { id: '3', vtip: 'I bought some shoes from a drug dealer. I dont know what he laced them with, but I was tripping all day!', user: 'user03', like: '30', dislike: '2' },
    { id: '4', vtip: 'Did you hear the news? FedEx and UPS are merging. They are going to go by the name Fed-Up from now on.', user: 'user04', like: '15', dislike: '8' },
    { id: '5', vtip: 'My daughter screeched, "Daaaaaad, you have not listened to one word I have said, have you!?" What a strange way to start a conversation with me...', user: 'user05', like: '90', dislike: '44' },
    { id: '6', vtip: 'My wife tried to unlatch our daughters car seat with one hand and said, "How do one armed mothers do it?" Without missing a beat I replied, "Single handedly."', user: 'user06', like: '38', dislike: '1' },
    { id: '7', vtip: 'When a dad drives past a graveyard: Did you know that is a popular cemetery? Yep, people are just dying to get in there!', user: 'user07', like: '66', dislike: '35' },
    { id: '8', vtip: 'My friend keeps saying "cheer up man it could be worse, you could be stuck underground in a hole full of water." I know he means well.', user: 'user08', like: '27', dislike: '18' },
    { id: '9', vtip: 'The fattest knight at King Arthurs round table was Sir Cumference. He acquired his size from too much pi.', user: 'user09', like: '42', dislike: '9' },
    ]
    }
  },
  methods: {
    zmenLike(id) {
      const likes = this.jokes.find(joke => joke.id === id);
      likes.like ++;
    },

    zmenDislike(id) {
      const dislikes = this.jokes.find(joke => joke.id === id);
      dislikes.dislike ++;
    }
  },
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
