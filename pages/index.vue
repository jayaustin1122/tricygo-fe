<template>
  <div>
    <v-carousel>
      <v-carousel-item
        v-for="(item, i) in items"
        :key="i"
        :src="item.src"
        cycle="true"
        reverse-transition="slide-transition"
        transition="slide-transition"
      ></v-carousel-item>
    </v-carousel>

    <div class="mb-11">
      <div class="ma-10 text-center">
        <h3>Welcome to our shop!</h3>
        <h1>Choose Sidecars</h1>
      </div>
      <div class="d-flex">
        <v-card
          v-for="item in products"
          :key="item.id"
          class="mx-5 boxbg rounded-card"
          max-width="344"
          outlined
        >
          <v-list-item three-line>
            <v-list-item-content>
              <v-list-item-title class="text-h5" style="color: white">{{
                item.name
              }}</v-list-item-title>
              <v-list-item-subtitle
                ><h4 style="color: white">
                  {{ item.price }}
                </h4></v-list-item-subtitle
              >
            </v-list-item-content>
            <v-list-item-avatar
              ><v-img max-height="100" max-width="100" :src="sample4"> </v-img
            ></v-list-item-avatar>
          </v-list-item>
          <v-card-actions>
            <v-btn outlined rounded text class="button" @click="create(item)">
              Order Now</v-btn
            >
          </v-card-actions>
        </v-card>
      </div>
      <!--End Cards-->
      <div style="margin-top: 200px">
        <h1 class="text-center mt-16 ms-6" style="margin-top: 300px">Login</h1>
        <v-form ref="form" v-model="valid" lazy-validation align-self="center">
          <v-row justify="center" align="center">
            <v-col cols="12" sm="6">
              <v-text-field
                v-model="user.email"
                label="Email"
                single-line
                outlined
              ></v-text-field>
              <v-text-field
                label="Password"
                single-line
                outlined
                type="password"
                hint="At least 8 characters"
              ></v-text-field>
              <div>
                <v-btn
                  rounded
                  color="#50C878"
                  style="margin-left: 170px; width: 120px"
                  >Login
                </v-btn>
                <v-btn
                  rounded
                  color="#44a6c6"
                  style="margin-left: 5px; width: 115px"
                  >Sign Up</v-btn
                >
              </div>
            </v-col>
          </v-row>
        </v-form>
        <div class="ma-10 text-center">
          <h1>TricyGo</h1>
        </div>
        <div class="d-flex mt-5">
          <v-img max-height="300" max-width="500" :src="logo"> </v-img>
          <h3 class="ml-4 mt-3 ma-10 text-center">
            Welcome to Tricygo, your one-stop shop for all things
            sidecar-related! At Tricygo, we specialize in providing an extensive
            range of high-quality products, including sidecars and various
            units, catering to your needs. Whether you're looking for galvanized
            or stainless steel units, we have you covered. Our store is designed
            to be a haven for sidecar enthusiasts, offering a diverse selection
            of products to suit different tastes and requirements. Step into our
            spacious showroom, and you'll be greeted by a vibrant and inviting
            atmosphere, showcasing our impressive collection.
          </h3>
        </div>
      </div>
    </div>
    <!--End login-->
    <div class="text-center" style="height: 700px">
      <h1 class="text-center ms-3" style="margin-top: 200px">Sign Up</h1>
      <v-form ref="form" v-model="valid" lazy-validation align-self="center">
        <v-row justify="center" align="center">
          <v-col cols="12" sm="5">
            <v-text-field label="Email" single-line outlined></v-text-field>
            <v-text-field
              label="Password"
              single-line
              outlined
              type="password"
              hint="At least 8 characters"
            ></v-text-field>
            <v-text-field label="Address" single-line outlined></v-text-field>
            <v-text-field
              label="Contact No."
              single-line
              outlined
            ></v-text-field>
            <div>
              <v-btn
                rounded
                color="#44a6c6"
                style="margin-left: 10px; width: 300px"
                >Create Account
              </v-btn>
            </div>
          </v-col>
        </v-row>
      </v-form>
    </div>
  </div>
</template>

<script>
export default {
  name: "IndexPage",
  layout: "simple",
  data() {
    return {
      products: [],
      user: {
        email: "",
        password: "",
      },
      items: [
        {
          src: require("~/assets/images/sample1.jpg"),
        },
        {
          src: require("~/assets/images/sample1.jpg"),
        },
        {
          src: require("~/assets/images/sample1.jpg"),
        },
        {
          src: require("~/assets/images/sample1.jpg"),
        },
      ],
      logo: require("~/assets/images/logo 2.png"),
      logo2: require("~/assets/images/delivery.jpg"),
      logo3: require("~/assets/images/logo3.png"),
      sample4: require("~/assets/images/sample1.jpg"),
    };
  },
  async mounted() {
    await this.$axios.get("api/v1/products/").then((res) => {
      this.products = res.data;
    });
  },
  methods: {
    async create(payload) {
      let order = {
        status: "pending",
        user_id: 1,
        product_id: payload.id,
      };
      await this.$axios.post("api/v1/orders/", order);
    },
  },
};
</script>

<style scoped>
h1 {
  color: #50c878;
}
.gg {
  align-items: center;
}
.boxbg {
  background-image: linear-gradient(#015e20, rgb(24, 201, 68));
}
.button {
  background-color: white;
}
.rounded-card {
  border-radius: 10px;
}
</style>
