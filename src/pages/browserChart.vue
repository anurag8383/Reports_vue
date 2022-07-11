<template>
  <div class="crafts">
    <div class="line">
      <h3 class="first">
        Browsers
        <hr class="hrline1" />
      </h3>
      <q-card bordered class="bg-white-9 my-card">
        <q-separator dark inset />
        <q-card-section class="chart-section">
          <label class="date">15 April - 12 May</label>
          <canvas id="myChart" width="350" height="200"></canvas>
        </q-card-section>
      </q-card>
    </div>
    <div class="line">
      <h3 class="first">
        Sessions
        <hr class="hrlines" />
      </h3>
      <q-card bordered class="bg-white-9 my-card">
        <q-separator dark inset />
        <q-card-section class="chart-section">
          <label class="date">15 April - 12 May</label>
          <canvas id="myChart9" width="350" height="200"></canvas>
        </q-card-section>
      </q-card>
    </div>
    <div class="line">
      <h3 class="first">
        Demographics
        <hr class="hrlinew" />
      </h3>
      <q-card bordered class="bg-white-9 my-card">
        <q-separator dark inset />
        <q-card-section class="chart-section">
          <label class="date">15 April - 12 May</label>
          <canvas id="myChart10" width="350" height="200"></canvas>
        </q-card-section>
      </q-card>
    </div>
  </div>
</template>

<script>
import Chart from "chart.js/auto";

export default {
  name: "demoGraph",
  mounted: function () {
    const ctx = document.getElementById("myChart");
    const myChart = new Chart(ctx, {
      type: "pie",
      data: {
        labels: ["15 April", "21 April"],
        datasets: [
          {
            label: "additional text",
            data: [508, 250],
            backgroundColor: ["#ffc0cb", "rgb(54, 162, 235)"],
            tension: 0.4,
            borderWidth: 2,
          },
        ],
      },
      options: {
        ticks: {
          min: 0,
          max: 500,
          stepSize: 250,
          fontColor: "#000",
          fontSize: 14,
        },
        elements: {
          point: {
            radius: 0,
          },
        },
        plugins: {
          legend: {
            display: true,
            position: "bottom",
            labels: {
              color: "rgb(255, 99, 132)",
            },
          },
        },
        responsive: false,
        chartArea: {
          backgroundColor: "rgba(251, 85, 85, 0.4)",
        },
      },
    });
    myChart;
    const ctx1 = document.getElementById("myChart9");
    const myChart9 = new Chart(ctx1, {
      type: "line",
      data: {
        labels: [
          "15 April",
          "21 April",
          "22 April",
          "29 April",
          "5 May",
          "12 May",
        ],
        datasets: [
          {
            label: "additional text",
            data: [258, 250, 300, 400, 350, 375],
            backgroundColor: "rgba(255, 99, 132, 0.2)",
            borderColor: "rgb(100,149,237)",
            tension: 0.4,
            borderWidth: 2,
          },
        ],
      },
      options: {
        scales: {
          y: {
            beginAtZero: true,
            grid: { display: false, drawBorder: false },
          },

          x: {
            grid: {
              offset: true,
              color: "rgb(135,206,235)",
              barThickness: 73,
              tickColor: "white",
              //  display: false, drawBorder: false
            },
          },
        },
        ticks: {
          min: 0,
          max: 500,
          stepSize: 250,
          fontColor: "#000",
          fontSize: 14,
        },
        elements: {
          point: {
            radius: 0,
          },
        },
        plugins: {
          legend: {
            display: false,
            labels: {
              color: "rgb(255, 99, 132)",
            },
          },
        },
        responsive: false,
        chartArea: {
          backgroundColor: "rgba(251, 85, 85, 0.4)",
        },
      },
    });
    myChart9;
    const ctx2 = document.getElementById("myChart10");
    const myChart10 = new Chart(ctx2, {
      type: "pie",
      data: {
        labels: ["15 April", "21 April"],
        datasets: [
          {
            label: "additional text",
            data: [258, 350],
            backgroundColor: ["#ffc0cb", "rgb(54, 162, 235)"],
            tension: 0.4,
            borderWidth: 2,
          },
        ],
      },
      options: {
        ticks: {
          min: 0,
          max: 500,
          stepSize: 250,
          fontColor: "#000",
          fontSize: 14,
        },
        elements: {
          point: {
            radius: 0,
          },
        },
        plugins: {
          legend: {
            display: true,
            position: "bottom",
            labels: {
              color: "rgb(255, 99, 132)",
            },
          },
        },
        responsive: false,
        chartArea: {
          backgroundColor: "rgba(251, 85, 85, 0.4)",
        },
      },
    });
    myChart10;
  },
};
</script>
<style scoped>
.crafts {
  display: flex;
  flex-direction: row;
  gap: 2em;
}
.line {
  width: 400px;
  height: 250px;
}
.date {
  font-size: 0.9rem;
  color: silver;
  margin-left: 40%;
  margin-bottom: 5%;
  /* justify-content: center;
  text-align: center; */
}
.first {
  font-size: 1.2rem;
  font-weight: 600;
  margin-left: 1rem;
}

.hrline {
  width: 12rem;
  height: 0.2rem;
  border: none;
  margin-left: -1%;
  margin-top: -2%;
  background-color: red;
}
.hrline1 {
  width: 5.5rem;
  height: 0.2rem;
  border: none;
  margin-left: -1%;
  margin-top: -2%;
  background-color: red;
}

.hrlines {
  width: 6rem;
  height: 0.2rem;
  border: none;
  margin-left: -1%;
  margin-top: -2%;
  background-color: red;
}
.hrlinew {
  width: 8rem;
  height: 0.2rem;
  border: none;
  margin-left: -1%;
  margin-top: -2%;
  background-color: red;
}
.my-card {
  border-radius: 3%;
}
</style>
