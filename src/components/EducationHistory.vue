<template>
  <section id="education">
    <h2>Education</h2>
    <div v-for="edu in education" :key="edu.degree" class="education-item">
      <h3>{{ edu.degree }}</h3>
      <p class="institution-period">{{ edu.institution }} | {{ edu.period }}</p>
    </div>
  </section>
</template>

<script>
export default {
  name: 'EducationHistory',
  data() {
    return {
      education: [
        {
          degree: 'Master in Data Science',
          institution: 'Eötvös Loránd University',
          location: 'Budapest, Hungary',
          period: 'September 2021 - January 2024'
        },
        {
          degree: 'Bachelor in Computer Science',
          institution: 'Khazar University',
          location: 'Baku, Azerbaijan',
          period: 'September 2017 - July 2021'
        }
      ]
    }
  }
}
</script>

<style scoped>
.education-item {
  margin-bottom: 1rem;
}

h3 {
  color: var(--dark-turquoise);
  margin-bottom: 0.25rem;
}

.institution-period {
  font-style: italic;
  color: var(--dark-gray);
  opacity: 0.7;
}
</style>