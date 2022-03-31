<!-- <template>
  <div>
    <Title>Nuxt 3 Example</Title>
    <nav>
        <ul>
            <li><NuxtLink to="/">Home</NuxtLink></li>
            <li><NuxtLink to="/about">About</NuxtLink></li>
            <li><NuxtLink to="/contact">Contact</NuxtLink></li>
        </ul>
    </nav>
    <slot />
  </div>
</template> -->

<template>
  <div class="bg-gray-300 min-h-screen text-gray-900">
    <Title>{{ title }}</Title>
    <nav class="bg-white shadow text-lg px-6 py-6">
      <div class="container mx-auto flex items-center justify-between px-6">
        <div>
          <NuxtLink to="/">Logo</NuxtLink>
        </div>
        <div>
          <ul class="flex space-x-12">
            <li>
              <NuxtLink to="/">Home</NuxtLink>
            </li>
            <li>
              <NuxtLink to="/about">About</NuxtLink>
            </li>
            <li>
              <NuxtLink to="/contact">Contact</NuxtLink>
            </li>
          </ul>
        </div>
      </div>
    </nav>
    <slot />
  </div>
</template>

<script setup>
const title = 'Nuxt 3 Blog'
</script>

<style>
.router-link-active {
  font-weight: bold;
}
</style>