<template>
    <div class="login-container">
      <div class="login-box">
        <div class="top-bar"></div>
        <h1 class="brand">LIEBHERR</h1>

        <h2 class="title">Sign In</h2>
        <p class="subtitle">Type your e-mail address and password.</p>
 
        <form @submit.prevent="handleSubmit">
          <div class="form-group">
            <label for="username">User name</label>
            <input
              id="username"
              v-model="username"
              type="text"
              placeholder="Enter your User name"
              class="input-field"
            />
          </div>
 
          <div class="form-group">
            <label for="password">Password</label>
            <input
              id="password"
              v-model="password"
              type="password"
              placeholder="Enter your Password"
              class="input-field"
            />
          </div>
 
          <a href="#" class="forgot-password">FORGOT PASSWORD?</a>
 
          <button type="submit" class="submit-button">SIGN IN</button>
        </form>
      </div>
    </div>
  </template>
 
  <script lang="ts">
  import { defineComponent, ref } from 'vue';
 
  export default defineComponent({
    name: 'LoginPage',
    setup() {
      const username = ref('');
      const password = ref('');
 
      const handleSubmit = () => {
        console.log('Username:', username.value);
        console.log('Password:', password.value);
        // Add your authentication logic here
      };
 
      return {
        username,
        password,
        handleSubmit,
      };
    },
  });
  </script>
 
  <style scoped>
  .login-container {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    background-color: #f4f4f4;
    font-family: Arial, sans-serif;
  }
 
  .login-box {
    background: #fff;
    padding: 2rem;
    border-radius: 8px;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    text-align: center;
    width: 400px;
  }
 
  .brand {
    color: #000000;
    font-size: 20px;
    font-weight: bold;
    margin-bottom: 1rem;
    text-align:  left ;
    
  }
  
 
  .title {
    font-size: 22px;
    font-weight: bold;
    margin-bottom: 0.5rem;
  }
 
  .subtitle {
    font-size: 14px;
    color: #666;
    margin-bottom: 2rem;
  }
 
  .form-group {
    margin-bottom: 1rem;
    text-align: left;
  }
 
  label {
    font-size: 14px;
    color: #333;
    display: block;
    margin-bottom: 0.5rem;
  }
 
  .input-field {
    width: 100%;
    padding: 0.5rem;
    border: 1px solid #ccc;
    border-radius: 4px;
    font-size: 14px;
  }
 
  .forgot-password {
    display: block;
    font-size: 10px;
    color: #161617;
    text-decoration: none;
    margin-bottom: 1rem;
    text-align: left;
  }
 
  .forgot-password:hover {
    text-decoration: underline;
  }
 
  .submit-button {
    width: 100%;
    padding: 0.75rem;
    background-color: #f7b500;
    color: #fff;
    border: none;
    border-radius: 4px;
    font-size: 16px;
    font-weight: bold;
    cursor: pointer;
  }
 
  .submit-button:hover {
    background-color: #e6a200;
  }
  </style>