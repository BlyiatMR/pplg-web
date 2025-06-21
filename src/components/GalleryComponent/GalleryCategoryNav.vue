<script setup>
defineProps(['categories', 'activeCategory'])
defineEmits(['update:activeCategory'])
</script>

<template>
  <nav>
    <ul class="flex flex-wrap sm:justify-center justify-start sm:gap-8 gap-y-2 gap-x-7">
      <li v-for="cat in categories" :key="cat.value">
        <button
          class="text-base font-semibold px-3 py-2 rounded-md transition-colors"
          :class="activeCategory === cat.value
            ? 'bg-[#926cd9] text-white'
            : 'text-slate-800 hover:bg-[#926cd9] hover:text-white'"
          @click="$emit('update:activeCategory', cat.value)"
        >
          {{ cat.label }}
        </button>
      </li>
    </ul>
  </nav>
</template>