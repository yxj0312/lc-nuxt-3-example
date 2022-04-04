<!-- <template>
<button class="px-5 py-2 border rounded hover:bg-teal-200">Hi 👏</button>
    <div>
        <div>This is the main page</div>
        <Counter />
    </div>
    <div>
        x: {{ x }}
        y: {{ y }}
    </div>
    <div>
        <ul>
            <li v-for="user in users" :key="user.id">
                {{ user.name }}
            </li>
        </ul>
    </div>

    <div>
        <ul>
            <li v-for="user in users2" :key="user.id">
                {{ user.name }}
            </li>
        </ul>
    </div>

    <div>
        <ul>
            <li v-for="user in users3" :key="user.id">
                {{ user.name }}
            </li>
        </ul>
    </div>

    <div>{{ user.name }}</div>

    <div>
        <h2>Weather</h2>
        <div>Description: {{ weather.weather[0].description }}</div>
        <div>Temperature: {{ weather.main.temp }} C</div>
    </div>
</template>

<script setup>
    const {x,y} = useMouse()

    const users = ref([])

    onMounted(()=> {
        fetch('https://jsonplaceholder.typicode.com/users')
        .then(response =>  response.json())
        .then(data =>  users.value = data)
    })

    const { data: users2 } = await useAsyncData('users2', () => $fetch('https://jsonplaceholder.typicode.com/users'))

    const { data: users3 } = await useFetch('https://jsonplaceholder.typicode.com/users')

    const { data: user } = await useFetch('https://jsonplaceholder.typicode.com/users/1', { pick: ['id', 'name', 'email'] })
    
    const { data : weather } = await useFetch('/api/weather')
</script> -->


<template>
    <div class="container mx-auto w-1/2 py-8 divide-y space-y-8 divide-gray-300">
        <PostItem v-for="post in posts" :key="post.id" :post="post"/>
    </div>
</template>

<script setup>
    const { data:posts } = await useFetch('http://127.0.0.1:8000/api/posts')
</script>