<template>
  <div class="home">
    <div class="hero">
      <h2>Welcome to the Student Info App</h2>
      <p>
        Keep track of students’ information easily and efficiently. View details like name, course, and year level at a glance.
      </p>
    </div>

    <div class="features">
      <div class="feature-card">
        <h3>📋 Manage Students</h3>
        <p>Easily view student information in a clean and organized interface.</p>
      </div>

      <div class="feature-card">
        <h3>💻 Modern Design</h3>
        <p>Interactive components and responsive design for smooth navigation.</p>
      </div>

      <div class="feature-card">
        <h3>⚡ Quick Access</h3>
        <p>Navigate seamlessly between pages using the header menu.</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600&display=swap');

.home {
  font-family: 'Poppins', sans-serif; /* NEW FONT */
  width: 90%;
  max-width: 1100px;
  margin: 40px auto;
  text-align: center;
  color: #333;
}

.hero {
  background: linear-gradient(135deg, #42b883, #38a1a0);
  color: white;
  padding: 40px 20px;
  border-radius: 12px;
  box-shadow: 0 6px 18px rgba(0, 0, 0, 0.08);
}

.hero h2 {
  font-weight: 600; /* slightly bold for headings */
  font-size: 2.2rem;
  margin-bottom: 15px;
}

.hero p {
  font-weight: 400;
  font-size: 1.1rem;
  line-height: 1.5;
}

.features {
  display: flex;
  gap: 20px;
  margin-top: 30px;
  flex-wrap: wrap;
  justify-content: center;
}

.feature-card {
  background: #ffffff;
  border-radius: 12px;
  padding: 20px;
  flex: 1 1 250px;
  max-width: 300px;
  box-shadow: 0 6px 15px rgba(0, 0, 0, 0.07);
  transition: transform 0.2s ease;
}

.feature-card:hover {
  transform: translateY(-5px);
}

.feature-card h3 {
  font-weight: 500;
  font-size: 1.2rem;
  margin-bottom: 10px;
  color: #42b883;
}

.feature-card p {
  font-weight: 400;
  font-size: 0.95rem;
  color: #555;
}
</style>

