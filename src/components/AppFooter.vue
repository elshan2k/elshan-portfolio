<template>
    <footer>
      <div class="footer-content">
        <p>&copy; {{ currentYear }} Elshan Gadimov. All rights reserved.</p>
        <div class="social-links">
          <a href="https://www.linkedin.com/in/elshan-gadimov-819ab6153/" target="_blank" aria-label="LinkedIn">
            <i class="fab fa-linkedin"></i>
          </a>
          <a href="https://github.com/elshan2k" target="_blank" aria-label="GitHub">
            <i class="fab fa-github"></i>
          </a>
        </div>
      </div>
    </footer>
  </template>
  
  <script>
  export default {
    name: 'AppFooter',
    computed: {
      currentYear() {
        return new Date().getFullYear();
      }
    }
  }
  </script>
  
  
  <style scoped>
  footer {
    background-color: var(--turquoise);
    color: var(--white);
    padding: 1rem 0;
    margin-top: 2rem;
  }
  
  .footer-content {
    display: flex;
    justify-content: space-between;
    align-items: center;
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 1rem;
  }
  
  .social-links a {
    color: var(--white);
    font-size: 1.5rem;
    margin-left: 1rem;
    transition: opacity 0.3s ease;
  }
  
  .social-links a:hover {
    opacity: 0.8;
  }
  </style>