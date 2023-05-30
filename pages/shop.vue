<template>
    <div>
      <div class=" mb-11">
        <div class="d-flex">
            <v-img class="ma-9" max-height="100" max-width="100" :src="logo"> </v-img>
                <div class="ma-10">
                     <h3>Welcome to our shop!</h3  >
                     <h1>Choose Sidecars</h1>
                </div>
             
        </div>
        <div class="d-flex">  
        <v-card class="mx-5 boxbg   rounded-card" width="500" outlined >
          <v-list-item three-line> 
                <v-list-item-content>
                    <v-list-item-title class="text-h5" style="color: white;">Galvanize</v-list-item-title>
                    <v-list-item-subtitle><h4 style="color: white;">₱40,000</h4></v-list-item-subtitle>
                    </v-list-item-content>
                    <v-list-item-avatar ><v-img max-height="100" max-width="200" :src="sample4"> </v-img></v-list-item-avatar>
                  </v-list-item>
                <v-card-actions>
              <v-btn outlined rounded text  class="button"> Order Now</v-btn>
            </v-card-actions>
        </v-card>
       



        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: "shop",
    layout: "simple",
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
    background-image: linear-gradient(#015e20, rgb(24, 201, 68));
  }
  .button{
    background-color: white;
  }
  .rounded-card{
      border-radius:10px;
  }
  
  </style>
  