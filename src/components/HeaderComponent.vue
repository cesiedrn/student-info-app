<template>
  <header class="header">
    <div class="container">
      <h1 class="logo">Student Info App</h1>
      <nav class="nav-links">
        <router-link to="/" exact-active-class="active-btn" class="btn-link">Home</router-link>
        <router-link to="/students" exact-active-class="active-btn" class="btn-link">Students</router-link>
      </nav>
    </div>
  </header>
</template>

<script>
export default {};
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600&display=swap');

.header {
  background: linear-gradient(90deg, #42b883, #38a1a0);
  color: white;
  padding: 15px 0;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
  position: sticky;
  top: 0;
  z-index: 100;
}

.container {
  width: 90%;
  max-width: 1100px;
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.logo {
  font-size: 1.8rem;
  font-weight: bold;
  font-family: 'Poppins', sans-serif; 
  letter-spacing: 1px;
}

.nav-links {
  display: flex;
  gap: 12px;
}

.btn-link {
  font-family: 'Poppins', sans-serif; /* NEW FONT */
  background-color: rgba(255, 255, 255, 0.2);
  border: 1px solid white;
  color: white;
  padding: 6px 18px;
  border-radius: 8px;
  text-decoration: none;
  font-weight: 500; /* matches Poppins weight */
  transition: background 0.3s, transform 0.2s;
}

.btn-link:hover {
  background-color: rgba(255, 255, 255, 0.4);
  transform: translateY(-2px);
}

.active-btn {
  background-color: white;
  color: #42b883;
  border: 1px solid #42b883;
}

 
@media (max-width: 600px) {
  .container {
    flex-direction: column;
    gap: 10px;
  }
}
</style>
