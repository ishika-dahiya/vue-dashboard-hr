<template>
  <div class="h-60 lg:h-70">
    <Line id="my-chart-id" :options="chartOptions" :data="chartData" />
  </div>
</template>

<script>
import { Line } from "vue-chartjs";
import {
  Chart as ChartJS,
  CategoryScale,
  LinearScale,
  PointElement,
  LineElement,
  Title,
  Tooltip,
  Legend,
  Filler,
} from "chart.js";

ChartJS.register(
  CategoryScale,
  LinearScale,
  PointElement,
  LineElement,
  Title,
  Tooltip,
  Legend,
  Filler
);

export default {
  name: "LineChart",
  components: { Line },
  data() {
    return {
      chartData: {
        labels: ["M", "T", "W", "T", "F", "S", "S", ""],
        datasets: [
          {
            label: false,
            backgroundColor: "rgba(168, 85, 247, 0.08)",
            borderColor: "#a855f7",
            fill: true,
            data: [0, 60, 36, 92, 38, 80, 36, 100],
          },
        ],
      },
      chartOptions: {
        responsive: true,
        maintainAspectRatio: false,
        scales: {
          x: {
            ticks: {
              padding: 20,
              align: "center",
            },
          },
          y: {
            beginAtZero: true,
            ticks: {
              stepSize: 40,
            },
            grid: {
              display: true,
              drawBorder: false,
            },
          },
        },
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
