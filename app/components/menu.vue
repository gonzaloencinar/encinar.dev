<template>
  <nav class="font-mono">
    <ul class="flex flex-col md:flex-row md:space-x-4">
      <li>
        <NuxtLink to="/" class="link">main</NuxtLink>
      </li>
      <li>
        <NuxtLink to="/about" class="link">about</NuxtLink>
      </li>
      <li>
        <NuxtLink to="/projects" class="link">projects</NuxtLink>
      </li>
      <li>
        <NuxtLink to="/blog" class="link">blog</NuxtLink>
      </li>
    </ul>
  </nav>
</template>

<style scoped>
.link {
  @apply p-1 hover:bg-gray-200 dark:hover:bg-gray-800 text-2xl md:text-base;
}
</style>
