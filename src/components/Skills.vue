<template>
    <section id="skills">
      <h2>Skills</h2>
      <ul class="skills-list">
        <li v-for="(skills, category) in skillCategories" :key="category">
          <strong>{{ category }}:</strong> {{ skills.join(', ') }}
        </li>
      </ul>
    </section>
</template>

<script>
export default {
  name: 'SkillsSection',
  data() {
    return {
      skillCategories: {
        'Programming Languages': ['Python', 'Java', 'SQL'],
        'Machine Learning': ['PyTorch', 'TensorFlow', 'Pandas', 'Regression & Classification', 'NLP', 'CV'],
        'Big Data & Cloud': ['PySpark', 'AWS'],
        'Databases': ['MySQL', 'NoSQL', 'InfluxDB', 'MongoDB'],
        'DevOps & Tools': ['Docker', 'Git', 'Grafana', 'Kafka']
      }
    }
  }
}
</script>

<style scoped>
.skills-list {
  list-style-type: none;
}

.skills-list li {
  margin-bottom: 1rem;
}

.skills-list strong {
  color: var(--dark-turquoise);
}
</style>