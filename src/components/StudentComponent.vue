<template>
  <div class="student-card">
    <div class="card-header">
      <h3>{{ name }}</h3>
      <span class="year-badge">Year {{ year }}</span>
    </div>

    <p class="course">{{ course }}</p>

    <button @click="toggleDetails" class="btn">
      {{ showDetails ? "Hide Details" : "View Details" }}
    </button>

    <div v-if="showDetails" class="details">
      <p>📘 Status: Enrolled</p>
      <p>🏫 Program: College of Computing</p>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    name: String,
    course: String,
    year: Number
  },
  data() {
    return {
      showDetails: false
    };
  },
  methods: {
    toggleDetails() {
      this.showDetails = !this.showDetails;
    }
  }
};
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600&display=swap');

.student-card {
  font-family: 'Poppins', sans-serif; /* NEW FONT */
  background: #ffffff;
  border-radius: 12px;
  padding: 16px;
  margin-bottom: 15px;
  box-shadow: 0 6px 18px rgba(0, 0, 0, 0.08);
  transition: transform 0.2s ease;
}

.student-card:hover {
  transform: translateY(-3px);
}

.card-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.card-header h3 {
  margin: 0;
  color: #333;
}

.year-badge {
  background: #42b883;
  color: white;
  padding: 4px 10px;
  border-radius: 20px;
  font-size: 0.85rem;
}

.course {
  margin: 8px 0 12px;
  color: #666;
}

.btn {
  background: #42b883;
  border: none;
  color: white;
  padding: 8px 14px;
  border-radius: 6px;
  cursor: pointer;
  font-size: 0.9rem;
}

.btn:hover {
  background: #369f6b;
}

.details {
  margin-top: 12px;
  padding-top: 10px;
  border-top: 1px solid #eee;
  color: #444;
}
</style>
