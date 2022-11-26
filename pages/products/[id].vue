<template>
    <div>
        <Head>
            <Title>Nux 3 | {{ product.title }}</Title>
            <Meta :name="'description'" :content="product.description"></Meta>
        </Head>
       <ProductDetails :product="product" />
    </div>
</template>

<script setup lang="ts">

definePageMeta({
    layout: 'products'
})

const { id } = useRoute().params

const {data: product}: {data: any} = await useFetch(`https://fakestoreapi.com/products/${id}`)

if(!product.value){
    throw createError({
        statusCode: 404,
        statusMessage: 'Product Not Found',
        fatal: true
    })
}

</script>

<style scoped>

</style>