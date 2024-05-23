<template>
  <div class="flex justify-evenly pt-2 md:pt-4 lg:pt-6">
    <div class="w-1/2 h-40 md:h-50 lg:h-60 pb-2">
      <Doughnut :data="chartData" :options="chartOptions" />
    </div>
    <div class="pb-4">
      <ul class="space-y-2 md:space-y-4 lg:space-y-6">
        <li class="flex items-center">
          <span class="w-4 h-4 bg-purple-600 rounded-full inline-block mr-2"></span> Agency
        </li>
        <li class="flex items-center">
          <span class="w-4 h-4 bg-yellow-500 rounded-full inline-block mr-2"></span> Social Media
        </li>
        <li class="flex items-center">
          <span class="w-4 h-4 bg-red-700 rounded-full inline-block mr-2"></span> Career Page
        </li>
        <li class="flex items-center">
          <span class="w-4 h-4 bg-lime-600 rounded-full inline-block mr-2"></span> Internal
        </li>
        <li class="flex items-center">
          <span class="w-4 h-4 bg-blue-200 rounded-full inline-block mr-2"></span> Job Boards
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
import { Doughnut } from "vue-chartjs";
import { Chart as ChartJS, ArcElement, Tooltip, Legend } from "chart.js";

ChartJS.register(ArcElement, Tooltip, Legend);

export default {
  name: "DoughnutChart",
  components: {
    Doughnut,
  },
  data() {
    return {
      chartData: {
        labels: [
          "Agency",
          "Career Page",
          "Job Boards",
          "Internal",
          "Social Media",
        ],
        datasets: [
          {
            label: false,
            backgroundColor: [
              "rgb(147 51 234)",
              "rgb(185 28 28)",
              "rgb(191 219 254)",
              "rgb(101 163 13)",
              "rgb(234 179 8)",
            ],
            data: [25, 13, 25, 12, 25],
            borderWidth: 0,
          },
        ],
      },
      chartOptions: {
        responsive: true,
        maintainAspectRatio: false,
        cutout: '70%',
        plugins: {
          legend: {
            display: false,
          },
        },
      },
    };
  },
};
</script>
