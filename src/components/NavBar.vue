<template>
  <nav class="navbar">
    <div class="navbar-container">
      <div class="navbar-left">
        <img src="@/assets/logo.png" alt="Logo" class="logo" />
      </div>
      <div class="navbar-right">
        <router-link to="/" class="nav-item">Home</router-link>
        <button class="login-button" @click="login">Log In</button>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'NavBar',
  methods: {
    login() {
      alert('Log In button clicked');
    },
  },
};
</script>

<style scoped>
.navbar {
  display: flex;
  justify-content: center; /* Pastikan konten di tengah */
  align-items: center;
  padding: 1rem;
  background-color: #f8f8f8;
  color: white;
  width: 100%;
  position: fixed;
  top: 0;
  left: 0;
  z-index: 1000;
}

.navbar-container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
  max-width: 1280px; 
  padding: 0 1rem;
}

.navbar-left .logo {
  height: 40px;
}

.navbar-right {
  display: flex;
  gap: 1.5rem;
  
}

.nav-item {
  color: black;
  text-decoration: none;
  font-size: 1rem;
  padding: 0.5rem 1rem;

}

.nav-item:hover {
  text-decoration: underline;
}

.login-button {
  background-color: #555;
  color: white;
  border: none;
  padding: 0.5rem 1rem;
  font-size: 1rem;
  cursor: pointer;
  border-radius: 4px;
}

.login-button:hover {
  background-color: #777;
}
</style>
