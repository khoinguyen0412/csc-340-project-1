<template>
    <div>
      <form @submit.prevent="handleSubmit">
        <!-- Name Input -->
        <div>
          <label for="name">Name:</label>
          <input type="text" id="name" v-model="formData.name" required />
        </div>
  
        <!-- Email Input -->
        <div>
          <label for="email">Email:</label>
          <input type="email" id="email" v-model="formData.email" required />
        </div>
  
        <!-- Submit Button -->
        <button type="submit">Submit</button>
      </form>
  
      <!-- Display Submitted Data -->
      <div v-if="submitted">
        <h3>Submitted Data:</h3>
        <p>Name: {{ formData.name }}</p>
        <p>Email: {{ formData.email }}</p>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        formData: {
          name: '',
          email: ''
        },
        submitted: false
      };
    },
    methods: {
      handleSubmit() {
        this.submitted = true;
        console.log('Form Data:', this.formData);
      }
    }
  };
  </script>
  
<style scoped>
  /* Add basic styles */
  form {
    margin: 20px;
  }
  
  div {
    margin-bottom: 10px;
  }
  
  label {
    display: block;
    margin-bottom: 5px;
  }
  
  input {
    width: 100%;
    padding: 8px;
    margin-bottom: 10px;
  }
  
  button {
    padding: 10px 15px;
    background-color: #42b983;
    color: white;
    border: none;
    cursor: pointer;
  }
  
  button:hover {
    background-color: #358a5b;
  }
  </style>
  