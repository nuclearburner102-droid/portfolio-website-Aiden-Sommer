<script setup lang="ts">
</script>

<template>
  <main class="about">
    <section class="hero">
      <p class="eyebrow">About Me</p>
      <h1>Who I Am</h1>
      <p>
        Hello, I’m Aiden Sommer. A future developer focused on building clean, reliable systems
        and improving my skills in modern web development.
      </p>
    </section>

    <section>
      <div>
        <h2>Background &amp; Interests</h2>
        <p>
          I’ve always been interested in how software solves real problems. Outside of coding I 
          enjoy using and tinkering with various computer systems and have come to enjoy learning
          more about the programming that makes them work.
        </p>
      </div>

      <div>
        <h2>Technical Skills</h2>
        <p>
          I’m actively building a solid foundation in learning various computer languages. Technologies
          and tools I’ve been working with include:
        </p>
        <ul>
          <li><strong>TypeScript</strong> — Writing safer and more maintainable code</li>
          <li><strong>Vite</strong> — Fast tooling and modern project setup</li>
          <li><strong>Python</strong> — Machine learning and data analysis</li>
          <li><strong>C#</strong> — Game development and backend programming</li>
        </ul>
      </div>

      <div>
        <h2>Career Goals</h2>
        <p>
          My goal is to become a professional developer who writes maintainable code and
          builds robust systems. I want to contribute to real products, work on my own projects,
          and keep growing both my technical skills and my ability to solve problems independently.
        </p>
        <p>
          In the near term I’m focused on mastering Vue and frontend fundamentals, while
          also expanding into broader concepts involving other languages. Longer term I’d like to take on
          roles where I can design reliable features and ship software that people can use every day.
        </p>
      </div>
    </section>
  </main>
</template>

<style scoped>
.about {
  max-width: 1100px;
  margin: 0 auto;
  padding: 2rem 1.5rem 4rem;
  font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
  color: #2c2929;
  line-height: 1.6;
}

.eyebrow {
  font-size: 0.9rem;
  font-weight: 600;
  text-transform: uppercase;
  letter-spacing: 0.08em;
  color: #216adf;
  margin-bottom: 0.75rem;
}
</style>