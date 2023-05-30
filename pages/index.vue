<template>
  <div>
    <div class="d-flex justify-center">
      <div class="mt-16">
        <h6>WELCOME TO</h6>
        <h1>MV TricyGO</h1>
        <h2>BEST SIDECAR IN TOWN</h2>
        <h2>STAINLESS OR GALVANIZED</h2>
        <v-btn rounded color="primary" dark>Order Now </v-btn>
      </div>
      <div class="mr-16">
        <v-img max-height="500" max-width="500" :src="logo"> </v-img>
      </div>
    </div>
    <div class="text-center mt-16 mb-16">
      <div>SHOP NOW</div>
      <h1>SHOP SIDECAR</h1>
      <div class="d-flex">
        <v-card class="mx-auto" max-width="344" outlined>
          <v-list-item three-line>
            <v-list-item-content>
              <v-list-item-title class="text-h5 mb-1">
                Stainless Sidecar
              </v-list-item-title>
              <v-list-item-subtitle>₱ 40,000</v-list-item-subtitle>
            </v-list-item-content>
          </v-list-item>

          <v-card-actions class="justify-center">
            <v-btn outlined rounded text> Button </v-btn>
          </v-card-actions>
        </v-card>
      </div>

      <div class="text-center mt-16">
        <div>GET NOW</div>
        <h1>ORDER WITH MV DELIVERY</h1>
        <div class="d-flex justify-center">
          <div>
            <v-img max-height="500" max-width="500" :src="logo2"> </v-img>
          </div>
          <div>
            <h2>Deliver or Pick-up Anytime</h2>
            <p>
              Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quidem
              possimus porro consequatur provident quaerat omnis maxime commodi
              consectetur blanditiis sunt? Lorem ipsum dolor sit amet,
              consectetur adipisicing elit. Quidem possimus porro consequatur
              provident quaerat omnis maxime commodi consectetur blanditiis
              sunt? Lorem ipsum dolor sit amet, consectetur adipisicing elit.
              Quidem possimus porro consequatur provident quaerat omnis maxime
              commodi consectetur blanditiis sunt?
            </p>
            <v-btn rounded color="primary" dark>Make Your Delivery Now </v-btn>
          </div>
        </div>
      </div>
      <div class="text-center mt-16">
        <div>OUR APP</div>
        <h1>DOWNLOAD APP WITH MV TRICYGO</h1>
        <div class="d-flex justify-center">
          <div>
            <h2>Today Deserve a Deliver</h2>
            <p>
              Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quidem
              possimus porro consequatur provident quaerat omnis maxime commodi
              consectetur blanditiis sunt? Lorem ipsum dolor sit amet,
              consectetur adipisicing elit. Quidem possimus porro consequatur
              provident quaerat omnis maxime commodi consectetur blanditiis
              sunt? Lorem ipsum dolor sit amet, consectetur adipisicing elit.
              Quidem possimus porro consequatur provident quaerat omnis maxime
              commodi consectetur blanditiis sunt?
            </p>
            <v-btn rounded color="primary" dark>Get App </v-btn>
          </div>
          <div class="ml-3">
            <v-img max-height="500" max-width="500" :src="logo3"> </v-img>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "IndexPage",
  layout: "simple",
  data() {
    return {
      logo: require("~/assets/images/logo 2.png"),
      logo2: require("~/assets/images/delivery.jpg"),
      logo3: require("~/assets/images/logo3.png"),
    };
  },
};
</script>

<style scoped></style>
