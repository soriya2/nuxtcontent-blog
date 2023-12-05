<script setup lang="ts">
const { slug } = useRoute().params;
</script>

<template>
  <article class="bg-gray-100 rounded-2xl">
    <ContentDoc :path="`/posts/${slug}`" v-slot="{ doc }">
      <img
        :src="doc.thumbnail"
        alt="images"
        class="w-full h-full object-cover"
      />
      <!-- Header -->
      <div class="text-start p-4">
        <h3 class="text-2xl font-semibold">{{ doc.title }}</h3>
        <p class="text-gray-700 text-sm mt-2">
          {{ doc.date }}
        </p>
      </div>
      <!-- Header -->
      <div class="p-4">
        <ContentRenderer :value="doc" />
      </div>
    </ContentDoc>
  </article>
</template>
