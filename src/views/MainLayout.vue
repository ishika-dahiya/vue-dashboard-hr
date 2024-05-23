<template>
  <div class="flex flex-col h-screen">
    <main class="flex-1 overflow-y-auto">
      <div>
        <div class="flex h-screen">
          <div class="lg:w-1/8">
            <SideMenu :toggleSidebar="toggleSidebar"/>
          </div>
          <div class="lg:w-7/8 w-full">
             <NavBar :toggleSidebar="toggleSidebar"/>
            <MainSection />
          </div>
        </div>
      </div>
    </main>
  </div>
</template>

<script>
import NavBar from "@/components/NavBar.vue";
import SideMenu from "@/components/SideMenu.vue";
import MainSection from "@/components/MainSection.vue";
export default {
  name: 'HelloWorld',
  components: {
    NavBar,
    SideMenu,
    MainSection,
  },
  data() {
    return {
      sidebarOpen: false,
    };
  },
  methods: {
    toggleSidebar() {
      this.sidebarOpen = !this.sidebarOpen;
    }
  }
}
</script>
