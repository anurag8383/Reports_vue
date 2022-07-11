<template>
  <div class="q-pa-md">
    <h3 class="first">
      Most Completed Course
      <hr class="hrline" />
    </h3>
    <q-table
      class="table"
      :rows="rows"
      :columns="columns"
      row-key="name"
      hide-bottom
    />
  </div>
</template>
<script>
/*eslint-disable*/
import { defineComponent } from "vue";

const columns = [
  {
    name: "Course Name",
    align: "center",
    label: "S.NO",
    field: "calories",
  },
  {
    name: "name",
    label: "Course Name",
    align: "left",
    field: (row) => row.name,
    format: (val) => `${val}`,
    sortable: true,
  },
  {
    name: "fat",
    label: "Enrolled",
    field: "fat",
  },
];
const rows = [
  {
    name: "Ethical Hacking Essentials(EHE)",
    calories: 159,
    fat: 6.0,
    carbs: 24,
    protein: 4.0,
    sodium: 87,
    calcium: "14%",
    iron: "1%",
  },
  {
    name: "Advanced Pen Testing",
    calories: 237,
    fat: 9.0,
    carbs: 37,
    protein: 4.3,
    sodium: 129,
    calcium: "8%",
    iron: "1%",
  },
  {
    name: "Advanced Ethical Hacking",
    calories: 262,
    fat: 16.0,
    carbs: 23,
    protein: 6.0,
    sodium: 337,
    calcium: "6%",
    iron: "7%",
  },
  {
    name: "Ethical Hacking Essentials(EHE)",
    calories: 305,
    fat: 3.7,
    carbs: 67,
    protein: 4.3,
    sodium: 413,
    calcium: "3%",
    iron: "8%",
  },
];
export default defineComponent({
  name: "courseName",
  setup() {
    return {
      columns,
      rows,
    };
  },
});
</script>
<style scoped>
.table {
  margin-top: 6%;
  width: 35rem;
  margin-right: -150px;
  /* margin-left:1rem; */
  height: 16rem;
}
.first {
  font-size: 1.2rem;
  font-weight: 600;
  margin-top: 13%;
  margin-left: 2rem;
}
.hrline {
  width: 14rem;
  height: 0.15rem;
  border: none;
  margin-left: -0.5%;
  margin-top: -2%;
  background-color: red;
}
</style>
