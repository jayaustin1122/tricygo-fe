<template>
    <div class="container justify-center">
      <v-card class="form-card">
        <v-card-title class="form-title">Create Account</v-card-title>
        <v-card-text>
          <v-form @submit.prevent="createAccount">
            <v-text-field v-model="username" label="Username" required class="custom-text-field"></v-text-field>
            <v-text-field v-model="email" label="Email" type="email" required class="custom-text-field"></v-text-field>
            <v-text-field v-model="password" label="Password" type="password" required class="custom-text-field"></v-text-field>
            <v-textarea v-model="address" label="Address" required class="custom-text-field"></v-textarea>
            <v-text-field v-model="contact" label="Contact Number" required class="custom-text-field"></v-text-field>
            <v-btn type="submit" color="primary">Create Account</v-btn>
          </v-form>
        </v-card-text>
        <v-card-text v-if="errorMessage" class="error">{{ errorMessage }}</v-card-text>
      </v-card>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        username: '',
        email: '',
        password: '',
        address: '',
        contact: '',
        errorMessage: ''
      };
    },
    methods: {
      createAccount() {
        // Perform account creation logic here
        if (this.username && this.email && this.password && this.address && this.contact) {
          // Successful account creation
          console.log('Account created successfully');
        } else {
          // Display error message if any field is missing
          this.errorMessage = 'Please fill in all fields';
        }
      }
    }
  };
  </script>
  
  <style scoped>
  .container {
    width: 500px;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
  }
 
  .form-card {
    max-width: 100%;
    width: 100%;
    background-color: #000000;
    border-radius: 10px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
    height: auto; /* Adjusted height */
  }
  
  .form-title {
    font-size: 24px;
    font-weight: bold;
    padding: 20px;
    text-align: center;
    background-color: #4CAF50;
    color: #ffffff;
    border-radius: 10px 10px 0 0;
  }
  
  .v-form > div {
    padding: 10px 20px; /* Adjusted padding */
  }
  
  .custom-text-field .v-input__control {
    background-color: #000000; /* Set black background color for text fields */
    color: #000000; /* Set white text color for text fields */
  }
  
  .v-btn {
    margin-top: 20px;
    width: 100%;
    border-radius: 5px;
  }
  
  .error {
    color: red;
    margin-top: 10px;
  }
  </style>
  