<script setup lang="ts"></script>

<template>
  <main class="home">
    <section class="hero">
      <div class="hero-content">
        <p class="eyebrow">Future Developer</p>
        <h1 class="name">Aiden Sommer</h1>
        <p class="tagline">
          Aspiring developer focused on building clean and reliable systems.
        </p>
        <p class="description">
          I’m currently deepening my skills in Vue and web development fundamentals. 
          My goal is to become a professional developer who writes maintainable code and create robust systems.
        </p>
      </div>
      <div class="hero-image">
        <img 
          src="/images/me.jpg" 
          alt="Professional photo of Aiden Sommer"
        />
      </div>
    </section>

    <section class="career">
      <h2>Building Toward a Career in Development</h2>
      <p>
        I’m committed to continuous learning and practical project work. 
        Right now I’m focused on mastering development with Vue and Vite, 
        while also exploring best practices that will help me become a well rounded developer.
      </p>
      <div class="focus-grid">
        <div class="focus-card">
          <h3>Frontend</h3>
          <p>Vue, modern CSS, responsive design, and clean layouts.</p>
        </div>
        <div class="focus-card">
          <h3>Tools & Workflow</h3>
          <p>Vite, Git, and building efficient development environments.</p>
        </div>
      </div>
    </section>
  </main>
</template>

<script setup>
</script>

<style scoped>
.home {
  max-width: 1100px;
  margin: 0 auto;
  padding: 2rem 1.5rem 4rem;
  font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
  color: #2c2929;
  line-height: 1.6;
}

.hero {
  display: flex;
  align-items: center;
  gap: 3.5rem;
  padding: 3rem 0 4rem;
  min-height: 70vh;
}

.hero-content {
  flex: 1;
}

.eyebrow {
  font-size: 0.9rem;
  font-weight: 600;
  text-transform: uppercase;
  letter-spacing: 0.08em;
  color: #3b82f6;
  margin-bottom: 0.75rem;
}

.name {
  font-size: 3rem;
  font-weight: 700;
  line-height: 1.15;
  margin: 0 0 1rem;
  color: #111;
}

.tagline {
  font-size: 1.25rem;
  font-weight: 500;
  color: #333;
  margin-bottom: 1.25rem;
}

.description {
  font-size: 1.05rem;
  color: #444;
  margin-bottom: 2rem;
  max-width: 34rem;
}

.hero-image {
  flex-shrink: 0;
}

.hero-image img {
  width: 280px;
  height: 280px;
  object-fit: cover;
  border-radius: 16px;
  box-shadow: 0 12px 30px rgba(0, 0, 0, 0.12);
}

.career {
  padding-top: 2rem;
  border-top: 1px solid #e5e7eb;
}

.career h2 {
  font-size: 1.75rem;
  margin-bottom: 1rem;
  color: #111;
}

.career > p {
  font-size: 1.05rem;
  color: #444;
  max-width: 42rem;
  margin-bottom: 2.5rem;
}

.focus-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
  gap: 1.5rem;
}

.focus-card {
  background: #f8fafc;
  border: 1px solid #e2e8f0;
  border-radius: 12px;
  padding: 1.5rem;
}

.focus-card h3 {
  margin: 0 0 0.5rem;
  font-size: 1.15rem;
  color: #1e40af;
}

.focus-card p {
  margin: 0;
  font-size: 0.95rem;
  color: #475569;
}

@media (max-width: 800px) {
  .hero {
    flex-direction: column-reverse;
    text-align: center;
    gap: 2.5rem;
    min-height: auto;
    padding: 2rem 0 3rem;
  }

  .hero-content {
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .description {
    max-width: 100%;
  }

  .name {
    font-size: 2.4rem;
  }

  .hero-image img {
    width: 220px;
    height: 220px;
  }

  .hero-buttons {
    justify-content: center;
  }
}

@media (max-width: 480px) {
  .name {
    font-size: 2rem;
  }

  .tagline {
    font-size: 1.1rem;
  }
}
</style>