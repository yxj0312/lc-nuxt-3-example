<template>
    <div class="container mx-auto w-1/2 py-8">
        <h3 class="text-3xl font-bold">
            <NuxtLink :to="`/posts/${post.id}`">{{post.title}}</NuxtLink>
        </h3>
        <div class="post-meta text-gray-700 flex items-center space-x-2">
            <div>{{post.created}}</div>
            <div>&middot;</div>
            <div>{{post.user.name}}</div>
        </div>
        <div class="post-content mt-4">{{post.body}}</div>
    </div>
</template>

<script setup>
const title = useState('title')
const route = useRoute()

const { data:post } = await useFetch(`http://127.0.0.1:8000/api/posts/${route.params.id}`)

</script>