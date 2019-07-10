<template>
  <div>
    <!-- button -->
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
          style="width: 60px;
    height: 60px; "
          v-model="fab"
          class="chat-btn"
          color="primary"
          dark
          fab
        >
          <v-icon large>message</v-icon>
          <v-icon>close</v-icon>
        </v-btn>
      </template>
    </v-speed-dial>

    <!-- first  background card -->
    <div v-show="!show">
      <v-container grid-list-sm text-xs-center style="margin-right: 1px;">
        <v-layout align-end justify-end row fill-height>
          <v-flex xs12 sm6 md5 lg4>
            <v-card dark class="intercom">
              <div class="card1">
                <v-layout column fill-height>
                  <div>
                    <div class="header">
                      <v-card-title class="main">
                        <div>
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
              <div style="height:157px;background-color: #fff;"></div>
            </v-card>

            <!-- fornt card -->
            <div>
              <div style="    padding: 26px 24px 24px;">
                <v-flex xs12 sm12 md12 lg6>
                  <v-layout row wrap>
                    <v-flex d-flex v-for="n in 6" :key="n">
                      <div>
                        <v-card class="card2" color="#ccc" dark>
                          <v-card-text>{{ lorem.slice(0, 70) }}</v-card-text>
                        </v-card>
                      </div>
                    </v-flex>
                  </v-layout>
                </v-flex>
              </div>
            </div>
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

      title: "Hi, we’re Intercom",
      subHeader:
        "We help your business grow by connecting you to your customers."
    };
  },
  methods: {}
};
</script>

<style>
.card2 {
  margin-bottom: 17px;
  background-color: #fff;
  border-radius: 3px;
  font-size: 14px;
  line-height: 1.4;
  color: #000;
  overflow: hidden;
  position: relative;
}
.main {
  align-items: baseline;
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  flex-direction: column;
}
.intercom {
  border-radius: 7px;
}
.v-speed-dial {
  position: absolute;
}
.image {
  width: 33.031;
  height: 31.969;
  max-width: 100%;
  max-height: 100%;
  display: block;
  margin: auto 0px;
}
.header {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: flex-start;
  overflow: hidden;
}
.sub-header {
  display: flex;
  color: rgba(255, 255, 255, 0.7);
  font-size: 1em;
}
.title {
  display: flex;
  color: #ffffff;
  font-size: 30px;
}
.card1 {
  height: 252px;
  background: linear-gradient(
    135deg,
    rgb(48, 71, 236) 0%,
    rgb(15, 34, 167) 100%
  );
}
.card {
  z-index: 2147483002;
  position: fixed;
  top: 0px;
  left: 0px;
  right: 0px;
  bottom: 0px;
  overflow-y: auto;
}
.chat-btn {
  background: linear-gradient(135deg, rgb(63, 84, 240) 0%, #2196f3 100%);
}
@media (min-width: 0) {
}
</style>
