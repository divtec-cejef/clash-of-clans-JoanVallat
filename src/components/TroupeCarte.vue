<script setup>
//Propriété
defineProps({
  troupe: {
    type: Object,
    required: true
  }
})

//Evénements
const emit = defineEmits(["former"]);

</script>

<template>
  <article>
    <header :style="`background: linear-gradient(60deg,#3B3B3B 0%, ${troupe.couleur} 100%);`">
      <img
          :src="troupe.image"
          :alt="troupe.nom">
    </header>
    <div
        class="level"
        :style="`color: ${troupe.couleur};`">
      Niveau {{ troupe.niveau }}
    </div>
    <h2 class="name">{{ troupe.nom }}</h2>
    <button
        :style="`background-color: ${troupe.couleur}`"
        @click="emit('former',troupe)"
    > Former
      <img src="/img/piece-or.png" alt="Former"></button>
    <p class="description">{{ troupe.description }}</p>
    <footer>
      <div class="training"
           :style="`background-color: ${troupe.couleur};`">
        <div>{{ troupe.formation }}<sup>sec</sup></div>
        <div>Formation</div>
      </div>
      <div class="speed"
           :style="`background-color: ${troupe.couleur};`">
        <div>{{ troupe.vitesse }}</div>
        <div>Vitesse</div>
      </div>
      <div class="cost"
           :style="`background-color: ${troupe.couleur};`">
        <div>{{ troupe.cout }}</div>
        <div>Coût</div>
      </div>
    </footer>
  </article>
</template>

<style scoped>

</style>