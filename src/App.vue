<template>
  <div id="app">
    <header>
      <h1>Elshan Gadimov</h1>
      <p>Machine Learning Engineer | Data Scientist</p>
    </header>
    <nav>
      <a href="#about">About</a>
      <a href="#skills">Skills</a>
      <a href="#experience">Experience</a>
      <a href="#education">Education</a>
      <a href="#projects">Projects</a>
    </nav>
    <main>
      <AboutMe />
      <Skills />
      <WorkExperience />
      <EducationHistory />
      <Projects />
    </main>
    <AppFooter />
  </div>
</template>

<script>

import AboutMe from './components/AboutMe.vue'
import Skills from './components/Skills.vue'
import WorkExperience from './components/WorkExperience.vue'
import EducationHistory from './components/EducationHistory.vue'
import Projects from './components/Project.vue'
import AppFooter from './components/AppFooter.vue'

export default {
  name: 'App',
  components: {
    AboutMe,
    Skills,
    WorkExperience,
    EducationHistory,
    Projects,
    AppFooter
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;700&display=swap');

:root {
  --turquoise: #40E0D0;
  --dark-turquoise: #00CED1;
  --light-gray: #f4f4f4;
  --dark-gray: #333;
  --white: #ffffff;
}

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  background-color: var(--white);
  color: var(--dark-gray);
  font-family: 'Roboto', sans-serif;
  line-height: 1.6;
}

#app {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 1rem;
}

header {
  background-color: var(--turquoise);
  color: var(--white);
  padding: 2rem;
  text-align: center;
  clip-path: polygon(0 0, 100% 0, 100% 85%, 0 100%);
}

h1 {
  font-size: 2.5rem;
  margin-bottom: 0.5rem;
}

header p {
  font-size: 1.2rem;
  opacity: 0.9;
}

nav {
  background-color: var(--white);
  padding: 1rem;
  position: sticky;
  top: 0;
  z-index: 1000;
  display: flex;
  justify-content: center;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

nav a {
  color: var(--dark-gray);
  text-decoration: none;
  margin: 0 1rem;
  font-weight: bold;
  transition: color 0.3s ease;
}

nav a:hover {
  color: var(--turquoise);
}

main {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 2rem;
  padding: 2rem 0;
}

section {
  background-color: var(--white);
  border-radius: 8px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  padding: 1.5rem;
  transition: transform 0.3s ease;
}

section:hover {
  transform: translateY(-5px);
}

h2 {
  color: var(--dark-turquoise);
  margin-bottom: 1rem;
  font-size: 1.5rem;
  border-bottom: 2px solid var(--turquoise);
  padding-bottom: 0.5rem;
}

@media (max-width: 768px) {
  main {
    grid-template-columns: 1fr;
  }
}
</style>