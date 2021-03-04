<template>
  <div class="about">
    <b-card class="container">
      <div class="bg-success text-light">
        <h1>นิติบุคคลที่เคยได้รับใบอนุญาตจากสำนักงาน</h1>
        <h1>หรือเคยจดทะเบียนประกอบธุรกิจกับสำนักงาน</h1>
      </div>
    </b-card>
    <!-- <input type="button" value="Load Data" @click="loadUser" /> -->
    <b-button variant="primary" value="Load Data" @click="loadUser"
      >Load Data</b-button
    >
    <div fields="left">
      <b-table striped hover :items="items"></b-table>
    </div>
    <!-- <ul v-for="amc in items" :key="amc.id">
      <li>id: {{ amc.unique_id }} , name: {{ amc.name_th }}</li>
    </ul> -->
  </div>
</template>
<script>
import axios from "axios";

export default {
  data() {
    return {
      items: null,
    };
  },
  methods: {
    loadUser() {
      let url =
        "https://api.sec.or.th/LicenseCheck/licensee/company?key=8f08b232ca5b41169d00211933d1e1ec";

      axios
        .get(url)
        .then((response) => {
          this.items = response.data;
        })
        .catch((err) => {
          console.log(err);
        });
    },
  },
};
</script>
