<template>
  <div class="w-full flex flex-row p-2 md:px-10 bg-white md:flex-col">
    <div class="flex flex-col md:flex-row items-center justify-between w-full p-2 divide-x-2 divide-gray-100">
      <div
        class="w-full md:w-1/3 flex flex-col text-center justify-center mb-4 md:mb-0"
      >
        <span class="text-gray-500 text-xs md:text-sm">Total Jobs</span>
        <span class="font-bold text-2xl md:text-4xl">482</span>
      </div>
      <div
        class="w-full md:w-1/3 flex flex-col text-center justify-center mb-4 md:mb-0"
      >
        <span class="text-gray-500 text-xs md:text-sm">Active Jobs</span>
        <span class="font-bold text-2xl md:text-4xl">128</span>
      </div>
      <div class="w-full md:w-1/3 flex flex-col text-center justify-center mb-4 md:mb-0">
        <span class="text-gray-500 text-xs md:text-sm"
          >Interview Scheduled</span
        >
        <span class="font-bold text-2xl md:text-4xl">48</span>
      </div>
    </div>

    <div
      class="flex flex-col md:flex-row justify-between w-full mb-1 gap-4 md:gap-10 mt-0 md:mt-2 p-2"
    >
      <div class="w-full md:w-1/4 flex items-center gap-3">
        <span class="font-bold text-lg md:text-2xl">48</span>
        <span class="text-gray-500 text-sm md:text-base">Total Candidates</span>
      </div>
      <div class="w-full md:w-1/4 flex items-center gap-3">
        <span class="font-bold text-lg md:text-2xl">12</span>
        <span class="text-gray-500 text-sm md:text-base"
          >Total Active Candidates</span
        >
      </div>
      <div class="w-full md:w-1/4 flex items-center gap-3">
        <span class="font-bold text-lg md:text-2xl">16</span>
        <span class="text-gray-500 text-sm md:text-base"
          >Archived Candidates</span
        >
      </div>
      <div class="w-full md:w-1/4 flex items-center gap-3">
        <span class="font-bold text-lg md:text-2xl">08</span>
        <span class="text-gray-500 text-sm md:text-base"
          >New Candidates (7 days)</span
        >
      </div>
    </div>
  </div>

  <div class="flex flex-col lg:flex-row w-full gap-10 py-5 md:px-10">
    <div class="w-full xl:w-2/3 flex flex-col gap-3 mx-2">
      <div class="flex items-center justify-between bg-white">
        <div class="flex gap-0 md:gap-1 text-gray-400 text-base">
          <button
            class="btn bg-white btn-sm md:btn-md rounded-full px-2 md:px-4 text-xs md:text-base item-center font-semibold"
          >
            Total
          </button>
          <button
            class="btn btn-sm md:btn-md bg-white rounded-full px-1 md:px-4 item-center border-none text-gray-400"
          >
            New Applicants
          </button>
          <button
            class="btn btn-sm md:btn-md border-none bg-white rounded-full px-1 md:px-4 item-center text-gray-400"
          >
            Interviewed
          </button>
        </div>
        <select
          class="select select-xs md:select-md rounded-full font-bold text-gray-500 border-1 border-gray-300 mr-3"
        >
          <option>This Week</option>
          <option>Option 1</option>
          <option>Option 2</option>
          <option>Option 3</option>
        </select>
      </div>
      <div class="md:px-0 h-60">
        <LineChart />
      </div>
    </div>
    <div class="w-full xl:w-1/3 flex flex-col border rounded-3xl mx-2">
      <div
        class="flex items-center justify-between p-3 md:pt-6 md:px-5 md:gap-6"
      >
        <span class="text-base font-semibold">Candidate Source Statistic</span>
        <select
          class="select select-sm rounded-full font-bold text-gray-500 border-1 border-gray-300 px-4"
        >
          <option>Select</option>
          <option>Option 1</option>
          <option>Option 2</option>
          <option>Option 3</option>
        </select>
      </div>
      <div class="md:px-0">
        <DoughnutChart />
      </div>
    </div>
  </div>

  <div class="flex flex-col lg:flex-row justify-between gap-5 py-5 md:px-10">
    <div class="w-full xl:w-1/2 flex flex-row justify-between gap-5 px-0">
      <div
        class="divide-y-2 divide-gray-200 w-full md:w-1/2 border-2 border-gray-200 rounded-lg p-2"
      >
        <div class="flex justify-between pt-5 pb-2 px-2">
          <span class="font-bold text-sm md:text-base">Recent Candidates</span>
          <button class="flex item-center text-purple-500 font-bold gap-2 text-sm md:text-base">
            See All
          </button>
        </div>
        <div class="flex flex-col gap-2 py-2 px-1 md:gap-4 md:py-4 md:px-2 md:m-1">
          <div class="flex justify-center items-center">
            <div
              class="h-6 w-6 md:h-10 md:w-10 rounded-full mr-4 bg-orange-100 text-center text-orange-500 pt-1 md:pt-2 text-xs md:text-sm font-bold"
            >
              CP
            </div>
            <div class="flex flex-col">
              <span class="text-gray-800 text-sm md:text-lg">Carla Press</span>
              <span class="text-gray-400 text-xs">Lorem ipsum dolor sit.</span>
            </div>
          </div>
          <div class="flex justify-center items-center">
            <div
              class="h-6 w-6 md:h-10 md:w-10 rounded-full mr-4 bg-orange-100 text-center text-orange-500 pt-1 md:pt-2 text-xs md:text-sm font-bold"
            >
              JD
            </div>
            <div class="flex flex-col">
              <span class="text-gray-800 text-sm md:text-lg">John Doe</span>
              <span class="text-gray-400 text-xs">Lorem ipsum dolor sit.</span>
            </div>
          </div>
          <div class="flex justify-center items-center">
            <div
              class="h-6 w-6 md:h-10 md:w-10 rounded-full mr-4 bg-orange-100 text-center text-orange-500 pt-1 md:pt-2 text-xs md:text-sm font-bold"
            >
              AD
            </div>
            <div class="flex flex-col">
              <span class="text-gray-800 text-sm md:text-lg">Alena Dias</span>
              <span class="text-gray-400 text-xs">Lorem ipsum dolor sit.</span>
            </div>
          </div>
        </div>
      </div>
      <div
        class="divide-y-2 divide-gray-300 w-full md:w-1/2 border-2 border-gray-300 rounded-lg p-2"
      >
        <div class="flex justify-between pt-5 pb-2 px-2">
          <span class="text-sm md:text-base font-bold">Most Viewed CV's</span>
          <button class="flex item-center text-purple-500 font-bold gap-2 text-sm md:text-base">
            See All
          </button>
        </div>
        <div class="flex flex-col pt-2 gap-5 md:m-1 md:pt-4">
          <div class="flex justify-between items-center">
            <div class="flex items-center">
              <span
                class="material-symbols-outlined h-6 w-6 md:h-10 md:w-10 rounded-full mr-2 pt-0.5 md:pt-1 font-bold bg-purple-100 text-center text-purple-600 text-sm md:text-lg"
              >
                upload_file
              </span>
              <span class="text-gray-800 text-sm md:text-lg font-semibold"
                >Omar Aminoff</span
              >
            </div>
            <span class="material-symbols-outlined text-purple-600">
              download
            </span>
          </div>
          <div class="flex justify-between items-center">
            <div class="flex items-center">
              <span
                class="material-symbols-outlined h-6 w-6 md:h-10 md:w-10 rounded-full mr-2 pt-0.5 md:pt-1 font-bold bg-purple-100 text-center text-purple-600 text-sm md:text-lg"
              >
                upload_file
              </span>
              <span class="text-gray-800 text-sm md:text-lg font-semibold"
                >Tiana Vaccaro</span
              >
            </div>
            <span class="material-symbols-outlined text-purple-600">
              download
            </span>
          </div>
          <div class="flex justify-between items-center">
            <div class="flex items-center">
              <span
                class="material-symbols-outlined h-6 w-6 md:h-10 md:w-10 rounded-full mr-2 pt-0.5 md:pt-1 font-bold bg-purple-100 text-center text-purple-600 text-sm md:text-lg"
              >
                upload_file
              </span>
              <span class="text-gray-800 text-sm md:text-lg font-semibold"
                >Aspen Carder</span
              >
            </div>
            <span class="material-symbols-outlined text-purple-600">
              download
            </span>
          </div>
        </div>
      </div>
    </div>

    <div class="w-full xl:w-1/2 mx-2">
      <HireFunnel />
    </div>
  </div>
</template>

<script>
import LineChart from "./LineChart.vue";
import DoughnutChart from "./DoughnutChart.vue";
import HireFunnel from "./HireFunnel.vue";

export default {
  name: "MainSection",
  components: {
    LineChart,
    DoughnutChart,
    HireFunnel,
  },
};
</script>
