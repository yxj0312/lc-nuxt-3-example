<template>
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
</template>

<script setup>
    const {x,y} = useMouse()

    const users = ref([])

    onMounted(()=> {
        fetch('https://jsonplaceholder.typicode.com/users')
        .then(response =>  response.json())
        .then(data =>  users.value = data)
    }) 
</script>