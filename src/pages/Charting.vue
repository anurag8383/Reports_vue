<template>
  <div>
    <div class="Prop">
      <canvas id="myChart2" width="0.01" height="0.1"></canvas>
    </div>
  </div>
</template>

<script>
// import { defineComponent } from "vue";

export default {
  name: "CharTing",
  mounted: function () {
    const ctx2 = document.getElementById("myChart2");
    const myChart2 = new Chart(ctx2, {
      type: "line",
      data: {
        labels: ["Red", "Blue", "Yellow", "Green", "Purple", "Orange"],
        datasets: [
          {
            label: "# of Votes",
            data: [12, 19, 3, 5, 2, 3],
            backgroundColor: "rgba(255, 99, 132, 0.2)",

            borderColor: "rgba(255, 99, 132, 1)",

            tension: 0.4,
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
};
</script>
