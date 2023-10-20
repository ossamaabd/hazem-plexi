<template>
  <section class="experiance pb-6">
    <v-img class="pa-10" src="../assets/experiance.jpg" lazy>
      <v-container>
        <h4 class="display-2 text-center">Section1</h4>

        <v-timeline

        >
          <div row>
            <v-col lg="6" xs="12" style="display: inline-block; height: 221px">
              <v-card style="display: inline-block" col-4 class="rounded-xl">
                <v-card-title >
                </v-card-title>
                <v-card-text>
                  <v-col
                    lg="4"
                    xs="12"
                    style="display: inline-block; height: 201px"
                  >
                    <v-img
                      class="mx-4"
                      style="max-height: 100%; max-width: 100%"
                      src="../assets/1.1.jpg"
                    ></v-img>
                  </v-col>
                  <v-col
                    lg="4"
                    xs="12"
                    style="display: inline-block; height: 201px"
                  >
                    <v-img
                      class="mx-4"
                      style="max-height: 100%; max-width: 100%"
                      src="../assets/1.2.jpg"
                    ></v-img>
                  </v-col>
                  <v-col
                    lg="4"
                    xs="12"
                    style="display: inline-block; height: 201px"
                  >
                    <v-img
                      class="mx-4"
                      style="max-height: 100%; max-width: 100%"
                      src="../assets/1.3.jpg"
                    ></v-img>
                  </v-col>
                </v-card-text>
              </v-card>
            </v-col>

            <v-col lg="6" xs="12" style="display: inline-block; height: 221px">
              <v-card style="display: inline-block" col-4 class="rounded-xl">
                <v-card-title >
                  Gifts and things for daily uses
                </v-card-title>
                <v-card-text>
                  We can provide gifts and different model as per customer's
                  request
                </v-card-text>
              </v-card>
            </v-col>
          </div>

          <div row >
            <v-col lg="6" xs="12" style="display: inline-block; height: 221px">
              <v-card style="display: inline-block" col-4 class="rounded-xl">
                <v-card-title >
                </v-card-title>
                <v-card-text style="margin-bottom:-27px;">
                  <v-col
                    lg="4"
                    xs="12"
                    style="display: inline-block; height: 101px"
                  >
                    <v-img
                      class="mx-4"
                      style="max-height: 100%; max-width: 100%"
                      src="../assets/2.1.jpg"
                    ></v-img>
                  </v-col>
                  <v-col
                    lg="4"
                    xs="12"
                    style="display: inline-block; height: 201px"
                  >
                    <v-img
                      class="mx-4"
                      style="max-height: 100%; max-width: 100%"
                      src="../assets/2.2.jpg"
                    ></v-img>
                  </v-col>
                  <v-col
                    lg="4"
                    xs="12"
                    style="display: inline-block; height: 201px"
                  >
                    <v-img
                      class="mx-4"
                      style="max-height: 100%; max-width: 100%"
                      src="../assets/2.3.jpg"
                    ></v-img>
                  </v-col>
                </v-card-text>
              </v-card>
            </v-col>

            <v-col lg="6" xs="12" style="display: inline-block; height: 221px">
              <v-card style="display: inline-block" col-4 class="rounded-xl">
                <v-card-title >
                  Advertisement banner
                </v-card-title>
                <v-card-text>
                  We are making different forms of lighting and regular
                  advertisement banner
                </v-card-text>
              </v-card>
            </v-col>
          </div>
          <div row>
            <v-col lg="6" xs="12" style="display: inline-block; height: 221px">
              <v-card style="display: inline-block" col-4 class="rounded-xl">
                <v-card-title >
                </v-card-title>
                <v-card-text>
                  <v-col
                    lg="4"
                    xs="12"
                    style="display: inline-block; height: 201px"
                  >
                    <v-img
                      class="mx-4"
                      style="max-height: 100%; max-width: 100%"
                      src="../assets/3.1.jpg"
                    ></v-img>
                  </v-col>
                  <v-col
                    lg="4"
                    xs="12"
                    style="display: inline-block; height: 201px"
                  >
                    <v-img
                      class="mx-4"
                      style="max-height: 100%; max-width: 100%"
                      src="../assets/3.2.jpg"
                    ></v-img>
                  </v-col>
                  <v-col
                    lg="4"
                    xs="12"
                    style="display: inline-block; height: 201px"
                  >
                    <v-img
                      class="mx-4"
                      style="max-height: 100%; max-width: 100%"
                      src="../assets/3.3.jpg"
                    ></v-img>
                  </v-col>
                </v-card-text>
              </v-card>
            </v-col>

            <v-col lg="6" xs="12" style="display: inline-block; height: 221px">
              <v-card style="display: inline-block" col-4 class="rounded-xl">
                <v-card-title >
                  indoor and outdoor decorations
                </v-card-title>
                <v-card-text>
                  False Ceilings, Examples of our work on false ceilings
                </v-card-text>
              </v-card>
            </v-col>
          </div>
        </v-timeline>
      </v-container>
    </v-img>
  </section>
</template>

<script>
export default {
  name: "Experiance",
  props: ["items"],
  components: {},
  data: () => ({
    drawer: null,

    experience: [
      {
        id:1,
        title: "Gifts and things for daily uses",
        date: "November 2021 - Present",
        institute: "Web Developer",
        decription:
          "We can provide gifts and different model as per customer's request",
      },
      {
        id:2,
        title: "Advertisement banner",
        date: "December 2020 - April 2021",
        institute: "Freelancer",
        decription:
          "We are making different forms of lighting and regular advertisement banner",
      },
      {
        id:3,
        title: "indoor and outdoor decorations",
        date: "March 2021 - August 2021",
        institute: "Freelancer",
        decription:
          "False Ceilings, Examples of our work on false ceilings",
      },
    ],
  }),
    methods: {
    getImagePath(id) {
      return `../assets/${id}.3.jpg`;
    },
  },
};
</script>
