<template>
    <div class="login">
      <h1>Login to Your Account</h1>
      <form>
        <div class="form-group">
          <label for="email">Email</label>
          <input type="email" id="email" v-model="email" required>
        </div>
        <div class="form-group">
          <label for="password">Password</label>
          <input type="password" id="password" v-model="password" required>
        </div>
        <button type="submit" @click.prevent="login">Login</button>
        <p v-if="error" class="error">{{ error }}</p>
      </form>
    </div>
  </template>
  
  <script>
  export default {
    name: 'App',
    data() {
      return {
        email: '',
        password: '',
        error: null
      }
    },
    methods: {
      login() {
        // perform login logic here, for example using axios to send login request to server
        axios.post('/api/login', { email: this.email, password: this.password })
          .then(response => {
            // if login successful, redirect to dashboard or home page
            this.$router.push('/')
          })
          .catch(error => {
            // if login failed, display error message
            this.error = error.response.data.message
          })
      }
    }
  }
  </script>
  
  <style scoped>
  .login {
    max-width: 500px;
    margin: 0 auto;
    padding: 20px;
    border: 1px solid #ccc;
  }
  
  .form-group {
    margin-bottom: 10px;
  }
  
  label {
    display: block;
    margin-bottom: 5px;
  }
  
  input[type="email"],
  input[type="password"] {
    display: block;
    width: 100%;
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 3px;
  }
  
  button[type="submit"] {
    background-color:#FFE3E8;
    color: #fff;
    border: none;
    border-radius: 3px;
    padding: 10px 20px;
    cursor: pointer;
  }
  
  .error {
    color: red;
    margin-top: 10px;
  }
  </style>
  