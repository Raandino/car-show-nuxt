<template>
     <Head>
        <Title>
           Ridin App
        </Title>
    </Head>
    <section class="flex max-w-5xl gap-4 w-fit flex-wrap mx-auto mt-5">
        <Card 
           v-for="(car, index) in cars"
            :id="car.id"
            :key="index"
            :brand="car.brand"
            :model="car.model"
            :year="car.year"
            :mileage="car.mileage"
            :price="car.price"
            :image_url="car.image_url"
        />
    </section>
</template>

<script setup >
    import Card from '../components/Card.vue';
    import cars from '../mockApi/cars.json'

    definePageMeta({
        layout: 'default'
    })


</script>

<style>
   
</style>