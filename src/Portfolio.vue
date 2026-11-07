<script setup lang="ts">
import { ref, onMounted } from 'vue'
const GITHUB_USERNAME = 'nuclearburner102-droid'

interface Repo {
  id: number
  name: string
  html_url: string
  description: string | null
  language: string | null
  updated_at: string
  fork: boolean}

const repos = ref<Repo[]>([])
const loading = ref(true)
const error = ref<string | null>(null)

function formatDate(iso: string): string {
  return new Date(iso).toLocaleDateString('en-US', {
    year: 'numeric',
    month: 'short',
    day: 'numeric',})}

async function fetchRepos() {
  loading.value = true
  error.value = null

  try {
    const response = await fetch(
      `https://api.github.com/users/${GITHUB_USERNAME}/repos?sort=updated&per_page=30`
    )

    const data: Repo[] = await response.json()
    repos.value = data.filter((repo) => !repo.fork)
  } catch (err) {
    error.value =
      err instanceof Error ? err.message : 'Something went wrong.'
    repos.value = []
  } finally {
    loading.value = false
  }
}

onMounted(() => {
  fetchRepos()
})
</script>

<template>
  <main class="portfolio">
    <section class="portfolio">
      <p class="eyebrow">My Work</p>
      <h1>Portfolio</h1>
      <p>
        Public repositories from my Github account.
      </p>
    </section>

    <div v-if="loading">
      <p>Loading repositories…</p>
    </div>

    <div v-else class="repo-grid">
      <article v-for="repo in repos" :key="repo.id" class="repo-card">
        <h2 class="repo-name">
          <a :href="repo.html_url" target="_blank" rel="noopener noreferrer">
            {{ repo.name }}
          </a>
        </h2>

        <p class="repo-text">
          {{ repo.description || 'No description provided.' }}
        </p>

        <div>
          <span v-if="repo.language" class="repo-language">
            {{ repo.language }}:
          </span>
          <span class="repo-text">
            Updated {{ formatDate(repo.updated_at) }}
          </span>
        </div>
      </article>
    </div>
  </main>
</template>

<style scoped>
.portfolio {
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

.repo-name {
  font-size: 1.5rem;
}

.repo-language {
  font-size: 1.05rem;
  font-weight: 600;
  color: #035ff3;
}

.repo-text {
  font-size: 1.05rem;
  font-weight: 600;
}

.repo-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  gap: 1.5rem;
}

.repo-card {
  background: #f8fafc;
  border: 1px solid #e2e8f0;
  border-radius: 12px;
  padding: 1.5rem;
  display: flex;
  flex-direction: column;
}
</style>