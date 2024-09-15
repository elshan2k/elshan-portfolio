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
    <AboutMe />
    <Skills />
    <WorkExperience />
    <EducationHistory />
    <Projects />
  </div>
</template>

<script>

import AboutMe from './components/AboutMe.vue'
import Skills from './components/Skills.vue'
import WorkExperience from './components/WorkExperience.vue'
import EducationHistory from './components/EducationHistory.vue'
import Projects from './components/Project.vue'

export default {
  name: 'App',
  components: {
    AboutMe,
    Skills,
    WorkExperience,
    EducationHistory,
    Projects
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

header {
  background-color: #34495e;
  color: white;
  padding: 2rem;
}

nav {
  background-color: #2c3e50;
  padding: 1rem;
}

nav a {
  color: white;
  text-decoration: none;
  margin: 0 1rem;
}

section {
  padding: 2rem;
}
</style>