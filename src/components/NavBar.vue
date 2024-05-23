<template>
  <div class="navbar bg-white md:pl-2 md:py-2 lg:pl-4 p-1 flex items-center flex-wrap mr-4">
    <div class="font-bold text-lg flex items-center">
      <button @click="toggleSidebar" class="xl:hidden flex items-center py-2 md:py-3.5 px-2 z-50">
        <span class="material-symbols-outlined text-sm md:text-xl lg:text-3xl">menu</span>
      </button>
      <span class="text-xs sm:text-base md:text-lg lg:text-xl">Hello, Welcome Sam!</span>
      <span class="material-symbols-outlined text-amber-600 px-1 text-sm sm:text-lg md:text-xl lg:text-2xl"> waving_hand </span>
    </div>

    <div class="buttons flex items-center space-x-2 md:space-x-4 ml-auto">
      <select
        class="select select-xs sm:select-sm md:select-md w-full rounded-full font-bold text-gray-500 border-1 border-gray-300 pr-6 mr-0 md:pr-16 lg:pr-32 md:mr-8 lg:mr-16 text-sm"
      >
        <option>Vanilla HR</option>
        <option>Option 1</option>
        <option>Option 2</option>
        <option>Option 3</option>
      </select>

      <button class="flex items-center relative">
        <span class="material-symbols-outlined text-gray-500 text-sm sm:text-base md:text-lg lg:text-xl">
          notifications
        </span>
        <span
          class="top-0 right-0 rounded-full text-red-600 text-xs absolute"
          style="transform: translate(-30%, -40%)"
          >&bullet;</span
        >
      </button>

      <button>
        <span class="text-indigo-500 font-bold text-xs sm:text-sm md:text-base lg:text-lg"> EB </span>
      </button>

      <button>
        <span class="material-symbols-outlined text-gray-500 text-sm sm:text-base md:text-lg lg:text-xl">
          keyboard_arrow_down
        </span>
      </button>
    </div>
  </div>
</template>

<script>
import { EventBus } from '../eventBus.js';

export default {
  methods: {
    toggleSidebar() {
      EventBus.emit('toggleSidebar');
    },
  },
};
</script>