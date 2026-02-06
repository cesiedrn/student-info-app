<template>
  <div class="students-page">
    <h2>Students Page</h2>

    <StudentComponent
      v-for="student in students"
      :key="student.id"
      :name="student.name"
      course="BS Information Technology"
      :year="4"
    />

    <p v-if="loading">Loading students...</p>
    <p v-if="error">{{ error }}</p>
  </div>
</template>

<script>
import StudentComponent from "../components/StudentComponent.vue";

export default {
  components: {
    StudentComponent
  },
  data() {
    return {
      students: [],
      loading: true,
      error: null
    };
  },
  mounted() {
    fetch("https://jsonplaceholder.typicode.com/users")
      .then(res => {
        if (!res.ok) {
          throw new Error("Failed to fetch data");
        }
        return res.json();
      })
      .then(data => {
        this.students = data;
        this.loading = false;
      })
      .catch(err => {
        this.error = err.message;
        this.loading = false;
      });
  }
};
</script>

<style scoped>
.students-page {
  font-family: 'Poppins', sans-serif; /* Apply new font */
  width: 90%;
  max-width: 1100px;
  margin: 40px auto;
  color: #333;
}

.students-page h2 {
  font-weight: 600;
  margin-bottom: 20px;
  color: #42b883;
}
</style>
