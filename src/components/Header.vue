<!-- src/components/Header.vue -->
<template>
  <header class="overlay-header">
    <div class="logo">
      <img src="@/assets/logo.gif" alt="Logo" />
    </div>
    <div class="nav-container">
      <nav class="nav-menu">
        <a href="#">Home</a>
        <a href="#">Shop</a>
        <a href="#">Features</a>
        <a href="#">Cart</a>
      </nav>
    </div>
    <button @click="navigateToLogin" class="login-button border border-white text-white px-4 py-1 rounded hover:bg-white hover:text-purple-800">
      Login
    </button>
  </header>
</template>

<script>
export default {
  name: "Header",
  methods: {
    navigateToLogin() {
      this.$router.push({ name: 'Login' });
    },
  },
};
</script>
  
  <style scoped>
  .overlay-header {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    background-color: rgba(0, 0, 0, 0.5);
    color: white;
    padding: 15px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    z-index: 1;
  }
  
  .logo img {
    width: 50px;
    height: auto;
  }
  
  .nav-container {
    flex-grow: 1;
    display: flex;
    justify-content: center;
  }
  
  .nav-menu {
    display: flex;
    gap: 20px;
  }
  
  .nav-menu a {
    color: white;
    text-decoration: none;
    font-size: 1.2rem;
    font-weight: 500;
    opacity: 0.8;
    transition: opacity 0.3s;
  }
  
  .nav-menu a:hover {
    opacity: 1;
  }
  
  .login-button {
    transition: background-color 0.3s, color 0.3s;
  }
  </style>
  