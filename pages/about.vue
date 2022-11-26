<template>
    <div>
        <h2>About</h2>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Pariatur vel tempora, fuga neque quis non voluptatum labore ut, dignissimos consequatur assumenda error quam distinctio quo quibusdam! Sint doloribus aliquam laudantium?</p>
        <p>Corporis voluptatibus id unde? A corporis nobis deleniti molestiae sequi voluptatibus explicabo ut doloremque nulla praesentium magnam placeat sit enim facilis totam, dignissimos aliquam dolores nisi temporibus repellat porro quae?</p>
        <div>
            {{ data }}
        </div>
    </div>
</template>

<script setup lang="ts">
    const data = await useFetch('/api/currency/GBP')
</script>

<style scoped>

</style>