<script setup>
import { ref } from 'vue'

const email = ref('')
const password = ref('')

const handleLogin = () => {
  console.log('Email:', email.value)
  console.log('Password:', password.value)
  alert('Login button clicked!')
}
</script>

<template>
  <div class="page">
    <div class="login-box">
      <h2>Login</h2>
      <form @submit.prevent="handleLogin">
        <div class="form-group">
          <label for="email">Email</label>
          <input id="email" type="email" v-model="email" required />
        </div>
        <div class="form-group">
          <label for="password">Password</label>
          <input id="password" type="password" v-model="password" required />
        </div>
        <button type="submit">Sign In</button>
      </form>
    </div>
  </div>
</template>

<style scoped>
.page {
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  
}

.login-box {
  background-color:rgb(80, 79, 79);
  padding: 2rem;
  border-radius: 16px;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.4);
  width: 100%;
  max-width: 400px;
  text-align: center;
  color: #fff;
}

h2 {
  margin-bottom: 1.5rem;
  font-size: 2rem;
  color: #61dafb;
}

.form-group {
  margin-bottom: 1.2rem;
  text-align: left;
}

label {
  display: block;
  margin-bottom: 0.5rem;
  font-weight: 500;
}

input {
  width: 100%;
  padding: 0.8rem;
  border: 1px solid #444;
  border-radius: 8px;
  background-color: #2a2a2a;
  color: white;
  font-size: 1rem;
}

input:focus {
  outline: none;
  border-color: #61dafb;
}

button {
  width: 100%;
  padding: 0.9rem;
  background-color: #4ade80;
  color: #121212;
  font-weight: bold;
  border: none;
  border-radius: 8px;
  font-size: 1rem;
  transition: background-color 0.3s;
  cursor: pointer;
}

button:hover {
  background-color: #22c55e;
}
</style>
