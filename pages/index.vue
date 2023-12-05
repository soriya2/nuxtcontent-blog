<script setup lang="ts"></script>

<template>
  <div>
    <ContentList
      path="/posts"
      v-slot="{ list }"
      :query="{
        draft: false,
        sort: [
          {
            date: -1,
          },
        ],
      }"
    >
      <div
        v-for="post in list"
        :key="post._path"
        class="blog-card bg-gray-100 rounded-2xl overflow-hidden mb-4"
      >
        <div class="h-[320px] relative">
          <img
            :src="post.thumbnail"
            class="w-full h-full object-cover absolute"
          />
        </div>
        <div class="p-4">
          <nuxt-link :to="`${post.slug}`" class="text-2xl font-semibold">{{
            post.title
          }}</nuxt-link>

          <p class="text-gray-500 font-light">post date: {{ post.date }}</p>
        </div>
      </div>
    </ContentList>
  </div>
</template>
