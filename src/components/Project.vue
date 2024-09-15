<template>
    <section id="projects">
      <h2>Projects</h2>
      <div v-for="project in projects" :key="project.title" class="project">
        <h3>{{ project.title }}</h3>
        <p class="description">{{ project.description }}</p>
        <div class="technologies">
          <span v-for="tech in project.technologies.slice(0, 3)" :key="tech" class="tech-tag">{{ tech }}</span>
        </div>
      </div>
    </section>
</template>

<script>
export default {
  name: 'ProjectSection',
  data() {
    return {
      projects: [
        {
          title: 'Streaming Framework',
          description: 'Designed and developed a streaming framework in a team project that detects anomalies in real-time.',
          technologies: ['Kafka', 'PySpark', 'InfluxDB', 'Grafana', 'Docker']
        },
        {
          title: 'Face Detection',
          description: 'Used PyTorch and designed 3 metrics to evaluate the accuracy of face detection models.',
          technologies: ['PyTorch', 'Computer Vision']
        }
      ]
    }
  }
}
</script>

<style scoped>
.project {
  margin-bottom: 1.5rem;
}

h3 {
  color: var(--dark-turquoise);
  margin-bottom: 0.25rem;
}

.description {
  margin-bottom: 0.5rem;
}

.technologies {
  display: flex;
  flex-wrap: wrap;
}

.tech-tag {
  background-color: var(--light-gray);
  color: var(--dark-turquoise);
  padding: 0.25rem 0.5rem;
  border-radius: 4px;
  margin-right: 0.5rem;
  margin-bottom: 0.5rem;
  font-size: 0.8rem;
}
</style>