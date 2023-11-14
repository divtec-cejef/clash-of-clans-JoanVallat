<script setup>

  defineProps({
  or: {
  type: Number,
  required: true
},
    troupes : {
      type: Array,
      required: true
    }
}  )

</script>

<template>
  <aside class="solde-or">
    <div>
      <img src="/img/piece-or-note.jpg" alt="Solde Or">
      {{ or }} pièces d'or
    </div>
    <div>
      <img src="/img/troupes-icon.png" alt="Troupes">
      {{ troupes.length }} troupes formées
    </div>
  </aside>
</template>

<style scoped>

</style>