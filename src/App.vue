<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App"/>
  <ContactView name="kamal"/>
  <TheCard name="saiful islam" >
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Eaque odio voluptatum animi natus soluta alias laudantium pariatur sit est accusantium ipsam, eum nostrum? Distinctio blanditiis sint ab impedit quas fugit quam dolor culpa labore excepturi dolorum reprehenderit voluptate placeat expedita asperiores sunt in laborum facere, sit veritatis suscipit qui tempore?</p>
  </TheCard>
   <TheCard name="title nme" >
    <template v-slot:info>
   <p>laudantium pariatur sit est accusantium ipsam, eum nostrum? Distinctio blanditiis sint ab impedit quas fugit quam dolor culpa labore excepturi dolorum reprehenderit voluptate placeat expedita asperiores sunt in laborum facere, sit veritatis suscipit qui tempore?</p>
    </template>
       
    </TheCard>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import ContactView from './components/ContactView.vue'
import TheCard from './components/TheCard.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    ContactView,
    TheCard
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
