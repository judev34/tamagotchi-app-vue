<!--
  Ce composant contient le formulaire de création d'un nouveau Tamagotchi.
  Il "emit" un évenement "addPet" quand le formulaire est soumit.
-->


<template>
    <div>
        <h1>TAMAGOTCHI APP</h1>
        <form action="">
        <label for="pet-name">Entrez un nom pour votre nouveau Tamagotchi : </label>
        <input v-model="petName" type="text" id="pet-name">
        <button v-on:click.prevent="onSubmitPetForm" type="submit">Créez un Tamagotchi</button>
        </form>
    </div>
</template>

<script>
export default {
    name : "FormTamagotchi",
    data() {
        return {
            petName: '',
            hungryLevel: 100,
            sleepLevel: 100,
            entertainmentLevel: 100
        }
    },
    /**
     * Cette méthode est apellé quand l'utilisateur click sur "Créer un Tamagotchi".
     * Cela va instancier un nouveau Tamagotchi avec ses Specs.
     */
    methods: {
        onSubmitPetForm: function() {
            const pet = {
                petName: this.petName,
                hungryLevel: this.hungryLevel,
                sleepLevel: this.sleepLevel,
                entertainmentLevel: this.entertainmentLevel
            }
            console.log(pet);

            /**
             * On reset l'input.
             */
            this.petName = ''

            // On va emettre l'évènement "addPet" qui va mettre à jour la liste des Tamagotchis 
            this.$emit('addPet', pet)
        }
    }
}
</script>

<style>

</style>