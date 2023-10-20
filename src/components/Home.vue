<template>
  <section class="intro-section my-5" id="home">
    <v-row class="align-center px-10" style="height: 22%">
      <v-col lg="6" xs="12" class="pa-6 font-weight-bold py-16">
        <h2 class="display-3">
         Hazem plexi for trading and making plexiglass
        </h2>
        <v-subheader>Acrylic panels / products tailor-made / marked row / laser cutting / Welcome request a catelog</v-subheader>
        <br />
        <br />

        <v-row class="mt-16 icons">
          <v-btn
            href="https://www.facebook.com/HazemZakaria.SY?mibextid=ZbWKwL"
            class="px-4 ma-3 my_icon"
            color="primary"
            target="_blank"
            fab
            small
          >
            <v-icon size="35">mdi-facebook</v-icon>
          </v-btn>
          <v-btn
            href="https://web.whatsapp.com/"
            class="px-4 ma-3 white--text my_icon"
            color="#01ff56"
            target="_blank"
            fab
            small
          >
            <v-icon size="35">mdi-whatsapp</v-icon>
          </v-btn>

        </v-row>
      </v-col>
      <v-col lg="6" xs="12">
        <v-img
          class="mx-4 my_image"
          style="border-radius: 50%"
          src="../assets/cover.jpg"
        ></v-img>
      </v-col>
    </v-row>
  </section>
</template>

<script>
export default {
  name: "Home",

  data: () => ({}),
};
</script>
