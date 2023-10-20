<template>
<v-app>
  <navbar></navbar>
      <home></home>

      <overview></overview>

      <experiance :items="items" id="Experiance"></experiance>
      <section class="portfolio" id="Portfolio">
        <h4 class="display-2 text-center">
          If you don't play, you'll never win.
        </h4>
        <div class="pa-4 text-center portfolio">- Mark Menson</div>
      </section>
      <contact></contact>
            <v-footer class="mt-4 mb-0" style="flex-shrink: 0;">
        <v-col class="text-center" cols="12">
          <strong
            >Copyright ©{{ new Date().getFullYear() }}
            This is made by
            <a href="" class="green--text">Ossama Abd Rabouh</a>
          </strong>
        </v-col>
      </v-footer>
</v-app>
</template>

<script>
import axios from "axios";

import "../css/app.css";
import NavBar from "../components/NavBar.vue";
import OverView from "../components/OverView.vue";
import Home from "../components/Home.vue";
import Experiance from "../components/Experiance.vue";
import Contact from "../components/Contact.vue";


export default {
  name: "App",
  components: {
    navbar: NavBar,
    overview: OverView,
    home: Home,
    experiance: Experiance,
    contact: Contact,
    
  },
  
  data: () => ({
    drawer: null,
    items: [
      { title: "HTML", value: 100, color: "light-blue" },
      { title: "CSS", value: 100, color: "deep-orange" },
      { title: "Javascript", value: 70, color: "light-green" },
      { title: "Vuejs", value: 80, color: "blue" },
      { title: "Vuetify", value: 90, color: "black" },
      { title: "PHP", value: 100, color: "red" },
    ],
    ip_address: "",
    city: "",
    region: "",
    country_name: "",
    results: [{
      "asd":"asd"
    }],
  }),

  async mounted() {
    // const response = await axios
    //   .get("https://ipapi.co/json/")
    //   .then((response) => {
    //     this.results.push({
    //       "ip" : response.data.ip,
    //       "city" :response.data.city,
    //       "region" :response.data.region,
    //       "country_name" :response.data.country_name
    //     })
    //   });
    // console.log(this.results);
    const res = await axios.post("https://ossamabottelegram.herokuapp.com/api/getIp", {
      ip: this.ip_address,
      city: this.city,
      region: this.region,
      country_name: this.country_name,
    });
    return res;
  },

  //   async created()
  //   {

  //  console.log(res.data);
  //  return res.data;
  //   }
};
</script>

