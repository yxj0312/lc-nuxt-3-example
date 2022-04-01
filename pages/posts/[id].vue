<template>
    <div class="container mx-auto w-1/2 py-8">
        <h3 class="text-3xl font-bold"><NuxtLink :to="`/posts/1`">Title of Post</NuxtLink></h3>
        <div class="post-meta text-gray-700 flex items-center space-x-2">
            <div>Feb 2, 2022</div>
            <div>&middot;</div>
            <div>Andre Madarang</div>
        </div>
        <div class="post-content mt-4">This is a dynamic route: {{ $route.params.id }}</div>
    </div>
</template>