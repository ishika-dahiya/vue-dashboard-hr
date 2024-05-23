<template>
  <div class="h-full">
    <!-- <button @click="toggleSidebar" class="xl:hidden flex items-center py-2 md:py-3.5 px-2">
      <span class="material-symbols-outlined text-sm md:text-xl lg:text-3xl">menu</span>
    </button> -->
    <div class="flex flex-grow flex-col h-full relative">
      <div
        :class="sidebarOpen ? 'block' : 'hidden'"
        class="absolute xl:relative xl:flex xl:flex-col bg-white md:border-r xl:border-gray-200 h-full z-40"
        @click.self="toggleSidebar"
      >
        <span class="text-lg md:text-2xl flex items-center font-semibold px-4 py-4 md:py-6">
          <span class="material-symbols-outlined rounded ml-4 md:ml-0 mr-0.5 text-indigo-500 text-xl md:text-3xl">
            filter_vintage
          </span> VanillaHR
        </span>
        <div class="flex flex-col cursor-pointer px-4 mt-2 md:mt-4 h-full">
          <label type="text" class="input input-sm md:input-md input-bordered flex items-center gap-1 md:gap-2 rounded-full">
            <span class="material-symbols-outlined w-6 h-6 opacity-40 text-base md:text-xl">search</span>
            <input type="text" class="grow" placeholder="Search" />
          </label>
          <div class="divide-y-2 divide-gray-300 md:mt-4 lg:mt-8 h-full text-gray-400">
            <div class="my-3">
              <div class="flex items-center px-4 py-2 cursor-pointer selected">
                <span class="material-symbols-outlined text-base md:text-xl mr-2">dashboard</span>
                <span class="text-xs md:text-sm seleted-text">Dashboard</span>
              </div>
              <div class="flex items-center px-4 py-2 cursor-pointer">
                <span class="material-symbols-outlined text-base md:text-xl mr-2">work</span>
                <span class="text-xs md:text-sm">Jobs</span>
              </div>
              <div class="flex items-center px-4 py-2 cursor-pointer">
                <span class="material-symbols-outlined text-base md:text-xl mr-2">assignment_ind</span>
                <span class="text-xs md:text-sm">Candidates</span>
              </div>
              <div class="flex items-center px-4 py-2 cursor-pointer">
                <span class="material-symbols-outlined text-base md:text-xl mr-2">calendar_month</span>
                <span class="text-xs md:text-sm">Calendar</span>
              </div>
            </div>
            <div class="my-3">
              <div class="flex items-center px-4 py-2 cursor-pointer">
                <span class="material-symbols-outlined text-base md:text-xl mr-2">account_circle</span>
                <span class="text-xs md:text-sm">Account</span>
              </div>
              <div class="flex items-center px-4 py-2 cursor-pointer">
                <span class="material-symbols-outlined text-base md:text-xl mr-2">receipt_long</span>
                <span class="text-xs md:text-sm">Billing</span>
              </div>
              <div class="flex items-center px-4 py-2 cursor-pointer">
                <span class="material-symbols-outlined text-base md:text-xl mr-2">settings</span>
                <span class="text-xs md:text-sm">Settings</span>
              </div>
              <div class="flex items-center px-4 py-2 cursor-pointer">
                <span class="material-symbols-outlined text-base md:text-xl mr-2">support_agent</span>
                <span class="text-xs md:text-sm">Support</span>
              </div>
            </div>
            <div class="flex flex-col justify-between my-3 text-gray-400">
              <div class="flex items-center px-4 py-2 cursor-pointer">
                <span class="material-symbols-outlined text-base md:text-xl mr-2">settings</span>
                <span class="text-xs md:text-sm">Admin</span>
              </div>
            </div>
          </div>
          <div class="flex items-center px-4 py-5 cursor-pointer text-gray-400 bg-white">
            <span class="material-symbols-outlined text-base md:text-xl mr-2">logout</span>
            <span class="text-xs md:text-sm">Logout</span>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { EventBus } from '../eventBus.js';

export default {
  data() {
    return {
      sidebarOpen: false,
    };
  },
  mounted() {
    EventBus.on('toggleSidebar', this.toggleSidebar);
  },
  beforeUnmount() {
    EventBus.off('toggleSidebar', this.toggleSidebar);
  },
  methods: {
    toggleSidebar() {
      this.sidebarOpen = !this.sidebarOpen;
    },
  },
};
</script>

<style scoped>
@media (min-width: 1280px) {
  .xl\\:hidden {
    display: none !important;
  }
}
.selected {
  @apply text-indigo-500 border-2 border-gray-100 rounded-full bg-gray-100;
}
.seleted-text {
  @apply text-gray-600 font-bold;
}
</style>
