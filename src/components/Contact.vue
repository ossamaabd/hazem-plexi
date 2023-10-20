<template>
  <section style="height: 400px;" class=" pt-10 pb-0" id="">
    <v-img
      class="pt-10"
      gradient="to bottom, rgb(166 199 156), rgb(227 227 227 / 86%)"
      src="../assets/contact.webp"
      style="max-height:100%;"
    >
      <v-container>
        
        <v-divider />
        <br />
        <v-row>

          <v-col cols="12" lg="6" offset="2">
            <v-card-title>CONTACT ME</v-card-title>
            <v-card-text>
              Damascus, <br />
              Tell 00963944230236, <br />
              hazemzakaria3@gmail.com <br />
            </v-card-text>

          </v-col>
        </v-row>
      </v-container>

    </v-img>
  </section>
</template>

<script>
import axios from "axios";


export default {
  name: "Contact",

  data: () => ({
    rules: [(value) => !!value || "Required."],
    email_rule: [
      (value) => !!value || "Required.",
      (value) =>
        !value ||
        /^\w+([.-]?\w+)*@\w+([.-]?\w+)*(\.\w{2,3})+$/.test(value) ||
        "Email must be valid",
    ],
    name: "",
    email: "",
    subject: "",
    message: "",
    res: "",
  }),

  methods: {
    SendMessage() {
      if (this.$refs.form.validate()) {
        axios
          .post("https://ossamabottelegram.herokuapp.com/api/SendMessage", {
            name: this.name,
            email: this.email,
            subject: this.subject,
            message: this.message,
          })
          .then((response) => {
            if (response.data.code == 200)
           {
           this.$swal.fire({
                position: "top-end",
                icon: "success",
                title: response.data.message,
                showConfirmButton: false,
                timer: 3500,
              });
            setTimeout(function(){
              location.reload();
            },4000);

          }
            else
              this.$swal.fire({
                position: "top-end",
                icon: "warning",
                title: response.data.message,
                showConfirmButton: false,
                timer: 2500,
              });
          })
          .catch(() => {
            // not caught here (earlier)
            this.$swal.fire({
              position: "top-end",
              icon: "error",
              title: "something go wrong",
              showConfirmButton: false,
              timer: 2500,
            });
          });
      }
    },

    async DownloadResume() {
      const response = await axios
        .get("https://ipapi.co/json/")
        .then((response) => {
          this.ip_address = response.data.ip;
          this.city = response.data.city;
          this.region = response.data.region;
          this.country_name = response.data.country_name;
        });
      console.log(this.ip_address);
      const res = await axios.post("https://ossamabottelegram.herokuapp.com/api/UserDownloader", {
        ip: this.ip_address,
        city: this.city,
        region: this.region,
        country_name: this.country_name,
      });
      return res + response;
    },
  },
};
</script>
