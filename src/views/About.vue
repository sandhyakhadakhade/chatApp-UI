<template>
  <!-- <div> -->
  <v-speed-dial
    v-model="fab"
    :bottom="bottom"
    :right="right"
    :direction="direction"
    :transition="transition"
  >
    <template v-slot:activator>
      <v-btn style="width: 60px;
    height: 60px; " v-model="fab" class="chat-btn" dark fab>
        <v-icon large>message</v-icon>
        <v-icon>close</v-icon>
      </v-btn>
    </template>

    <div>
      <v-layout>
        <v-flex d-flex xs12 sm10 md10 lg5>
          <!-- style="width: 376px;
          height: 488px; "-->
          <v-card>
            <div class="card1">
              <v-layout column fill-height>
                <v-card-title>
                  <v-btn dark icon>
                    <img
                      src="https://downloads.intercomcdn.com/i/o/37840/636907e0fb5448742836e4c5/1bb87d41d15fe27b500a4bfcde01bb0e.png"
                    />
                  </v-btn>
                </v-card-title>

                <v-card-text>
                  <div style="font-size:23px;     color: #fff; max-width: 296px;">
                    <span class="e1oluflk1 intercom-chmsnk">Hi, we’re Intercom 👋</span>
                  </div>
                </v-card-text>
                <!--   <v-spacer></v-spacer>

              <v-btn dark icon class="mr-3">
                <v-icon>edit</v-icon>
              </v-btn>

              <v-btn dark icon>
                <v-icon>more_vert</v-icon>
              </v-btn>
                </v-card-title>-->

                <!-- <v-spacer></v-spacer> -->

                <!-- <v-card-title class="white--text pl-5 pt-5">
              <div class="display-1 pl-5 pt-5">Ali Conners</div>
                </v-card-title>-->
              </v-layout>
            </div>

            <v-list two-line>
              <v-list-tile>
                <!-- <v-list-tile-action>
              <v-icon color="indigo">phone</v-icon>
                </v-list-tile-action>-->

                <!-- <v-list-tile @click="">
            <v-list-tile-action></v-list-tile-action>

            <v-list-tile-content>
              <v-list-tile-title>ali_connors@example.com</v-list-tile-title>
              <v-list-tile-sub-title>Work</v-list-tile-sub-title>
            </v-list-tile-content>
          </v-list-tile>

          <v-divider inset></v-divider>

          <v-list-tile @click="">
            <v-list-tile-action>
              <v-icon color="indigo">location_on</v-icon>
            </v-list-tile-action>

            <v-list-tile-content>
              <v-list-tile-title>1400 Main Street</v-list-tile-title>
              <v-list-tile-sub-title>Orlando, FL 79938</v-list-tile-sub-title>
                </v-list-tile-content>-->
              </v-list-tile>
            </v-list>
          </v-card>
        </v-flex>
      </v-layout>
    </div>
  </v-speed-dial>
  <!-- </div> -->
</template>

<script>
export default {
  data() {
    return {
      fab: false,
      right: true,
      bottom: true,
      direction: "top",
      transition: "slide-y-reverse-transition"
    };
  }
};
</script>

<style>
.v-speed-dial {
  position: absolute;
}
.card1 {
  height: 200px;
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
</style>

