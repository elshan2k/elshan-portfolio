<template>
  <section id="experience">
    <h2>Work Experience</h2>
    <div v-for="job in jobs" :key="job.title" class="job">
      <h3>{{ job.title }}</h3>
      <p class="company-period">{{ job.company }} | {{ job.period }}</p>
      <ul>
        <li>{{ job.responsibilities[0] }}</li>
      </ul>
    </div>
  </section>
</template>

<script>
export default {
  name: 'WorkExperience',
  data() {
    return {
      jobs: [
        {
          title: 'Machine Learning Engineer',
          company: 'Flash Payments',
          period: 'December 2022 - Present',
          location: 'Sydney, Australia (Remote)',
          responsibilities: [
            'Designed and built an end-to-end ML system for detecting suspicious payments, reducing manual work',
            'Analyzed historical data and proposed changes that decreased manual work of compliance by half',
            'Developed a GenAI-based service that optimized tasks by 20 times'
          ]
        },
        {
          title: 'Data Science Student Researcher',
          company: 'ELTE - Data Science Department',
          period: 'February 2022 - December 2022',
          location: 'Budapest, Hungary',
          responsibilities: [
            'Collected Cyber Security position data from LinkedIn and applied text mining, clustering, and topic modeling',
            'Implemented Text Summarization with abstractive and extractive models for Lecture Notes'
          ]
        },
        {
          title: 'Machine Learning Engineer',
          company: 'e-Gov Development Center',
          period: 'May 2021 - September 2021',
          location: 'Baku, Azerbaijan',
          responsibilities: [
            'Developed an ensemble model for customer waiting time prediction',
            'Designed and implemented scalable API for the developed ML model'
          ]
        },
        {
          title: 'Machine Learning Trainee',
          company: 'ABB Innovation',
          period: 'December 2020 - May 2021',
          location: 'Baku, Azerbaijan',
          responsibilities: [
            'Developed ML model to predict bank customer loan default probability',
            'Analyzed fashion product reviews and predicted numeric ratings and recommendations'
          ]
        },
        {
          title: 'Software Developer Intern',
          company: 'Food Safety Agency',
          period: 'January 2020 - April 2020',
          location: 'Baku, Azerbaijan',
          responsibilities: [
            'Designed and implemented an application to automate transactions between lab and stock'
          ]
        }
      ]
    }
  }
}
</script>

<style scoped>
.job {
  margin-bottom: 1.5rem;
}

h3 {
  color: var(--dark-turquoise);
  margin-bottom: 0.25rem;
}

.company-period {
  font-style: italic;
  color: var(--dark-gray);
  opacity: 0.7;
  margin-bottom: 0.5rem;
}

ul {
  list-style-type: none;
}

li::before {
  content: '•';
  color: var(--turquoise);
  display: inline-block;
  width: 1em;
  margin-left: -1em;
}
</style>