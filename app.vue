<template>
  <div class="max-w-3xl px-4 mx-auto">
    <!-- Header -->
    <header class="mt-8 mb-4 flex justify-between items-end">
      <div>
        <nuxt-link to="/">
          <h1 class="text-2xl font-semibold">Personal Blog</h1>
        </nuxt-link>
        <p class="text-gray-400">Learn Programming Easily</p>
      </div>

      <Btn>Hire me</Btn>
    </header>
    <!-- Header -->

    <!-- Main Content -->
    <NuxtPage />
  </div>
</template>
