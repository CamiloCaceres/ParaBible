<script setup lang="ts">
const vulgata = {
  name: 'Vulgata',
  text: 'et ait : Faciamus hominem ad imaginem et similitudinem nostram : et praesit piscibus maris, et volatilibus caeli, et bestiis, universaeque terrae, omnique reptili, quod movetur in terra. Et creavit Deus hominem ad imaginem suam : ad imaginem Dei creavit illum, masculum et feminam creavit eos.',
  quote: 'Gn 1, 26-27',
}

const septuaginta = {
  name: 'Septuaginta',
  text: 'et ait : Faciamus hominem ad imaginem et similitudinem nostram : et praesit piscibus maris, et volatilibus caeli, et bestiis, universaeque terrae, omnique reptili, quod movetur in terra. Et creavit Deus hominem ad imaginem suam : ad imaginem Dei creavit illum, masculum et feminam creavit eos.',
  quote: 'Gn 1, 26-27',
}
const bibles = [vulgata, septuaginta, vulgata]

</script>

<template>
  <div class="flex justify-center space-x-8">
    <div v-for="bible in bibles" :key="bible.name">
      <DisplayBible :name="bible.name" :text="bible.text" :quote="bible.quote" />
    </div>
  </div>
  <button class="my-5 rounded-full p-2 bg-green-500 text-green-700 dark:text-green-100 dark:bg-green-600 shdow-lg hover:bg-green-400 hover:text-green-600 transition transform hover:rotate-180">
    <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
      <path stroke-linecap="round" stroke-linejoin="round" d="M12 4v16m8-8H4" />
    </svg>
  </button>
</template>
