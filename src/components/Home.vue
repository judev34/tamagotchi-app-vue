<template>
  <div class="hello">
    <form-tamagotchi></form-tamagotchi>
    <pet-list></pet-list>
  </div>
</template>

<script>
import FormTamagotchi from './FormTamagotchi.vue'
import PetList from './PetList.vue'

export default {
  name: 'Home',
  components: {
    FormTamagotchi,
    PetList
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>

* {
  box-sizing: border-box;
}

body {
  margin: 0;
  padding: 0
}

</style>
