<script setup>
    import {
        NavigationMenu,
        NavigationMenuItem,
        NavigationMenuList,
        NavigationMenuLink
    } from './ui/navigation-menu';
    import Button from './ui/button/Button.vue';
    import { ref } from 'vue';
    import { Menu } from 'lucide-vue-next';

    const isOpen = ref(false)

    const toggleMenu = () => {
        isOpen.value = !isOpen.value
    }

</script>

<template>
    <section>
        <NavigationMenu class="bg-gray-300 rounded-xl p-2 hidden sm:flex">
            <NavigationMenuList>

                <NavigationMenuItem>
                    <NavigationMenuLink class="text-sm">Sobre mim</NavigationMenuLink>
                </NavigationMenuItem>

                <NavigationMenuItem>
                    <NavigationMenuLink class="text-sm">Experiencias</NavigationMenuLink>
                </NavigationMenuItem>
                
                <NavigationMenuItem>
                    <NavigationMenuLink class="text-sm">Tecnologias</NavigationMenuLink>
                </NavigationMenuItem>

                <NavigationMenuItem>
                    <NavigationMenuLink class="text-sm">Projetos</NavigationMenuLink>
                </NavigationMenuItem>

            </NavigationMenuList>
        </NavigationMenu>

        <Button
            class="sm:hidden hover:bg-gray-300 fixed top-5 left-5 z-50 p-2 bg-transparent"
            @click="toggleMenu"
        >
            <Menu color="black"/>
        </Button>

        <div
            v-if="isOpen"
            class="md:hidden fixed top-0 left-0 w-3/4 h-full bg-white dark:bg-[rgba(0,0,0,0.8)] backdrop-blur-md shadow-xl z-40 p-6 flex flex-col transition-all"
        >
            <div class="my-10">
                <div>
                    <a href="#project" @click="toggleMenu"><p class="text-lg">Sobre Mim</p></a>
                </div>

                <div>
                    <a href="#experience" @click="toggleMenu"><p class="text-lg">Experiências</p></a>
                </div>

                <div>
                    <a href="#stack" @click="toggleMenu"><p class="text-lg">Tecnologias</p></a>
                </div>

                <div>
                    <a href="#projects" @click="toggleMenu"><p class="text-lg">Projetos</p></a>
                </div>
            </div>
        </div>
    </section>
</template>