<template>
  <div>
    Anurag SIngh
    <canvas id="myChart" width="100" height="100"></canvas>
  </div>
</template>


<script>
import { defineComponent } from "vue";

export default defineComponent({
  name: "AreaChart",
  mounted: function () {
    const ctx = document.getElementById("myChart");
    const myChart = new Chart(ctx, {
      type: "Area",
      data: {
        labels: ["Running", "Swimming", "Eating", "Cycling"],
        datasets: [
          {
            fill: {
              target: "origin",
              above: "rgb(255, 0, 0)",
              below: "rgb(0, 0, 255)",
            },
          },
        ],
      },
      options: {
        scales: {
          y: {
            beginAtZero: true,
          },
        },
      },
    });
    myChart;
  },
});
</script>
