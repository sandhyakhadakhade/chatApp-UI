<template>
  <div>
    <v-speed-dial
      v-model="fab"
      :bottom="bottom"
      :right="right"
      :direction="direction"
      :transition="transition"
    >
      <template v-slot:activator>
        <v-btn
          @click="show = !show"
          style="width: 60px; height: 60px; "
          v-model="fab"
          class="chat-btn"
          dark
          fab
        >
          <v-icon large>message</v-icon>
          <v-icon>close</v-icon>
        </v-btn>
      </template>
    </v-speed-dial>

    <!-- first  card  class=" scroll-y"-->
    <div v-show="!show">
      <v-container
        id="scroll-target"
        grid-list-sm
        text-xs-center
        style="margin-right: 1px; max-height: 400px;"
      >
        <v-layout align-end justify-end row fill-height>
          <v-flex xs12 sm5 md4 lg4>
            <v-card dark class="intercom">
              <div class="card1">
                <v-layout column fill-height>
                  <div>
                    <div class="header">
                      <v-card-title class="main">
                        <div style="    padding-left: 10px">
                          <img
                            style="width: 40px;"
                            src="https://downloads.intercomcdn.com/i/o/37840/636907e0fb5448742836e4c5/1bb87d41d15fe27b500a4bfcde01bb0e.png"
                          />
                        </div>
                        <div>
                          <br />
                          <div class="title">
                            <span style="font-size: 25px; max-width: 296px;">{{ title}} 👋</span>
                          </div>
                          <div class="sub-header">{{ subHeader }}</div>
                        </div>
                      </v-card-title>
                    </div>
                  </div>
                </v-layout>
              </div>
              <div class="sub-card"></div>
            </v-card>
          </v-flex>
        </v-layout>
      </v-container>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      lorem: `Lorem ipsum dolor sit amet, mel at clita quando. Te sit oratio vituperatoribus, nam ad ipsum posidonium mediocritatem, explicari dissentiunt cu mea. Repudiare disputationi vim in, mollis iriure nec cu, alienum argumentum ius ad. Pri eu justo aeque torquatos.`,
      show: true,
      fab: false,
      right: true,
      bottom: true,
      direction: "top",
      transition: "slide-y-reverse-transition",
      search: "Find an answer yourself",

      title: "Hi, we’re Intercom",
      subHeader:
        "We help your business grow by connecting you to your customers.",
      conversion: [
        {
          heading: "Your conversations",
          operator: "Operator",
          date: "1d ago",
          message: "Operator: Hi there 👋 What brings you to Intercom today?"
        }
      ]
    };
  },
  methods: {}
};
</script>

<style>
@import "../styles/dashboard.css"

</style>
