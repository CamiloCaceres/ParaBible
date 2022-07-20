<script setup lang="ts">
import {
  Combobox,
  ComboboxInput,
  ComboboxOption,
  ComboboxOptions,
} from '@headlessui/vue'

// change this with the actual Bible names
const people = [
  'Durward Reynolds',
  'Kenton Towne',
  'Therese Wunsch',
  'Benedict Kessler',
  'Katelyn Rohan',
]
const selectedPerson = ref(people[0])
const query = ref('')

const filteredPeople = computed(() =>
  query.value === ''
    ? people
    : people.filter((person) => {
      return person.toLowerCase().includes(query.value.toLowerCase())
    }),
)
</script>

<template>
  <div class="h-96 w-80 shadow-2xl rounded-lg mx-auto bg-gray-700">
    <h2>Chose pericope to compare:</h2>

    <Combobox v-model="selectedPerson">
      <ComboboxInput class="bg-gray-800" @change="query = $event.target.value" />
      <ComboboxOptions>
        <ComboboxOption
          v-for="person in filteredPeople"
          :key="person"
          :value="person"
        >
          {{ person }}
        </ComboboxOption>
      </ComboboxOptions>
    </Combobox>
  </div>
</template>
