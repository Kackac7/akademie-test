<template>
    <div class="joke">
      <div class="joke-body">
        <img class="joke-user" v-bind:src="`/images/users/${user}.png`"/>
        <p class="joke-text"> {{vtip}}</p>
      </div>
      <div class="joke-likes">
        <button class="btn-like btn-up" v-on:click="zmenLike"></button>
        <span class="likes-count likes-up">{{like}}</span>

        <button class="btn-like btn-down" v-on:click="zmenDislike"></button>
        <span class="likes-count likes-down">{{dislike}}</span>
      </div>
    </div>
</template>
<script>

export default {
    
    props: ['id', 'vtip', 'user', 'like', 'dislike'],

methods: {
        dajLike() {
            this.$emit('give-like', this.id)
        },
        dajDislike() {
            this.$emit('give-dislike', this.id)
        }
}
}
</script>
<style>

</style>