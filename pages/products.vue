<template>
  <div class="d-flex">
  <div>
    <h1>AVAILABLE SIDECARS</h1>
    <div class="d-flex mt-3">
      <v-card class="mx-5 boxbg   rounded-card mt-3" max-width="344" outlined >
        <v-list-item three-line> 
              <v-list-item-content>
                  <v-list-item-title class="text-h5" style="color: white;"><h2>Half Stainless</h2></v-list-item-title>
                  <v-list-item-subtitle><h3 style="color: white;">₱40,000</h3></v-list-item-subtitle>
                  </v-list-item-content>
                  <v-list-item-avatar ><v-img max-height="50" max-width="50" :src="sample4"> </v-img></v-list-item-avatar>
                </v-list-item>
              <v-card-actions>
          </v-card-actions>
      </v-card> 

      <v-card class="mx-5 boxbg   rounded-card mt-3" max-width="344" outlined >
        <v-list-item three-line> 
              <v-list-item-content>
                  <v-list-item-title class="text-h5" style="color: white;"><h2>Half Stainless</h2></v-list-item-title>
                  <v-list-item-subtitle><h3 style="color: white;">₱40,000</h3></v-list-item-subtitle>
                  </v-list-item-content>
                  <v-list-item-avatar ><v-img max-height="50" max-width="50" :src="sample4"> </v-img></v-list-item-avatar>
                </v-list-item>
              <v-card-actions>
          </v-card-actions>
      </v-card>

  
    </div>
    <div class="d-flex">
      <v-card class="mx-5 boxbg   rounded-card mt-3" max-width="344" outlined >
        <v-list-item three-line> 
              <v-list-item-content>
                  <v-list-item-title class="text-h5" style="color: white;"><h2>Half Stainless</h2></v-list-item-title>
                  <v-list-item-subtitle><h3 style="color: white;">₱40,000</h3></v-list-item-subtitle>
                  </v-list-item-content>
                  <v-list-item-avatar ><v-img max-height="50" max-width="50" :src="sample4"> </v-img></v-list-item-avatar>
                </v-list-item>
              <v-card-actions>
          </v-card-actions>
      </v-card>

      <v-card class="mx-5 boxbg   rounded-card mt-3" max-width="344" outlined >
        <v-list-item three-line> 
              <v-list-item-content>
                  <v-list-item-title class="text-h5" style="color: white;"><h2>Half Stainless</h2></v-list-item-title>
                  <v-list-item-subtitle><h3 style="color: white;">₱40,000</h3></v-list-item-subtitle>
                  </v-list-item-content>
                  <v-list-item-avatar ><v-img max-height="50" max-width="50" :src="sample4"> </v-img></v-list-item-avatar>
                </v-list-item>
              <v-card-actions>
          </v-card-actions>
      </v-card>

     
    </div>
    <div class="d-flex">
      <v-card class="mx-5 boxbg   rounded-card mt-3" max-width="344" outlined >
        <v-list-item three-line> 
              <v-list-item-content>
                  <v-list-item-title class="text-h5" style="color: white;"><h2>Half Stainless</h2></v-list-item-title>
                  <v-list-item-subtitle><h3 style="color: white;">₱40,000</h3></v-list-item-subtitle>
                  </v-list-item-content>
                  <v-list-item-avatar ><v-img max-height="50" max-width="50" :src="sample4"> </v-img></v-list-item-avatar>
                </v-list-item>
              <v-card-actions>
          </v-card-actions>
      </v-card>

      <v-card class="mx-5 boxbg   rounded-card mt-3" max-width="344" outlined >
        <v-list-item three-line> 
              <v-list-item-content>
                  <v-list-item-title class="text-h5" style="color: white;"><h2>Half Stainless</h2></v-list-item-title>
                  <v-list-item-subtitle><h3 style="color: white;">₱40,000</h3></v-list-item-subtitle>
                  </v-list-item-content>
                  <v-list-item-avatar ><v-img max-height="50" max-width="50" :src="sample4"> </v-img></v-list-item-avatar>
                </v-list-item>
              <v-card-actions>
          </v-card-actions>
      </v-card>
    </div>
   
  </div>
  <div>
      
      <div class="text-center">
        <h2 style="margin-top: 50px;">Add New Product</h2>
        <v-form ref="form" v-model="valid" lazy-validation align-self="center">
          <v-row justify="center" align="center">
            <v-col>
              <v-text-field width="300px" margin-top="30px" label="Product Name" single-line outlined></v-text-field>
              <v-text-field width="300px" margin-top="30px" label="Description" single-line outlined></v-text-field>
              <v-text-field width="300px" margin-top="30px" label="Amount" single-line outlined></v-text-field>
            
            <div >
              <v-btn rounded color="#44a6c6"   style="margin-left: 10px; margin-top: 10px; width: 400px;">ADD </v-btn>
              <v-btn rounded color="green"  style="margin-left: 10px; margin-top: 10px; width: 400px;">Edit </v-btn>
              <v-btn rounded color="red"  style="margin-left: 10px; margin-top: 10px; width: 400px;">Delete </v-btn>
            </div>
            </v-col>
        </v-row>
        </v-form>
        </div>
    </div>
  </div>
</template>


<script>
export default {
  name: "DashboardPage",
  data() {
    return {
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
};
</script>
<style scoped>
h1{
  color: #50C878;
}
.gg{
  align-items: center;
}
.boxbg{
  background-image: linear-gradient(#05b941, rgb(24, 201, 68));
}
.button{
  background-color: white;
}
.rounded-card{
    border-radius:10px;
}

</style>