<template>
    <div>
      <form @submit.prevent="handleSubmit">
        <!-- Name Input -->
        <div>
          <label for="name">Name:</label>
          <input type="text" id="name"  required />
        </div>
  
        <!-- Email Input -->
        <div>
          <label for="email">Email:</label>
          <input type="email" id="email"  required />
        </div>
  
        <!-- Submit Button -->
        <button type="submit">Submit</button>
      </form>
  
      <!-- Display Submitted Data -->
    </div>
  </template>
  
  <script>
  export default {
    methods: {
      handleSubmit() {
        this.submitted = true;
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
  