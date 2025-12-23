<script setup>
    import {
        Card,
        CardHeader,
        CardTitle,
        CardDescription,
        CardContent,
        CardFooter
    } from './ui/card/';

    const journey = [
        {
            title: 'Primeiro Contato com Programação',
            period: '2022 - 2023',
            description: 'Meu primeiro contato com programação aconteceu em 2022, quando tive minhas primeiras experiências com HTML e CSS. A partir desse momento, passei a me interessar cada vez mais pela área e decidi ingressar no curso técnico de Desenvolvimento de Sistemas para aprofundar meus conhecimentos.'
        },
        {
            title: 'Curso técnico',
            location: '| EEEP Jaime da Cunha Rebouças',
            period: '2023.2 - 2025.1',
            description: 'Ao iniciar o curso, fui introduzido aos fundamentos da lógica de programação e, em seguida, estudei minha primeira linguagem: Python. No segundo semestre de 2024, começamos a explorar Programação Web e Programação Orientada a Objetos, ampliando minha base técnica e meu entendimento sobre desenvolvimento de software.'
        },
        {
            title: 'Aprofundamento',
            period: '2023 - 2025',
            description: 'Entre o segundo semestre de 2024 e meados de 2025, busquei expandir ainda mais meu conhecimento por meio de crsos externos. Foi nesse período que tive contato com minha primeira linguagem de programação voltada ao desenvolvimento web: JavaScript. Esse aprofundamento me motivou a estudar de forma contínua e começar a construir projetos mais sólidos.'
        },
        {
            title: 'Estágio e primeiros projetos',
            location: '| EEEP Jaime da Cunha Rebouças',
            period: '2025.2',
            description: 'No segundo semestre de 2025, iniciei meu estágio supervisionado obrigatório, oferecido pela EEEP. Durante essa experiência, consegui consolidar tudo o que havia aprendido até então e aplicar na prática, desenvolvendo novos projetos e adquirindo diversas habilidades adicionais, tanto técnicas quanto profissionais.'
        }
    ]
</script>
<template>
    <section>
        <div class="grid grid-cols-1 gap-6">
            <div v-for="item in journey">
                <Card>
                    <CardHeader>
                        <CardTitle>{{ item.title }} </CardTitle>
                        <CardDescription>{{ item.period }} {{ item.location }}</CardDescription>
                    </CardHeader>


                    <CardContent class="text-xs text-justify">
                        {{ item.description }}
                    </CardContent>
                </Card>
            </div>
        </div>
    </section>
</template>