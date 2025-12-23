<script setup>
    import {
        Card,
        CardHeader,
        CardTitle,
        CardDescription,
        CardContent,
        CardFooter
    } from './ui/card/';

    const stack = [
        {
            name: 'HTML',
            url: ''
        },
        {
            name: 'CSS',
            url: ''
        },
        {
            name: 'JavaScript',
            url: ''
        },
        {
            name: 'Vue.js',
            url: ''
        },
        {
            name: 'TailwindCSS',
            url: ''
        }
    ]
</script>

<template>
    <section>
        <div>
            <h1>Tecnologias que uso</h1>
        </div>

        <div>
            <Card class="flex">
                <CardContent v-for="item in stack">
                    <img :src="item.url" alt="">
                    <p>{{ item.name }}</p>
                </CardContent>
            </Card>
        </div>
    </section>
</template>