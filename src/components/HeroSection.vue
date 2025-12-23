<script setup>
import {
    Avatar,
    AvatarFallback,
    AvatarImage
} from './ui/avatar';
import Button from './ui/button/Button.vue';
</script>

<template>
    <section>
        <div class="flex flex-col text-justify items-center justify-center gap-4">
            <div>
                <Avatar class="w-50 h-50">
                    <AvatarImage src="/img/profile.png" alt="@radix-vue"  />
                    <AvatarFallback>CN</AvatarFallback>
                </Avatar>
            </div>
    
            <div class="flex flex-col space-y-6 ">

                <div class="place-items-center">
                    <p class="text-3xl sm:text-4xl font-extrabold font-sans">
                        JOAO VITOR
                    </p>
                    <p class="text-md">
                        Desenvolvedor Front-end
                    </p>
                </div>

                <div class="w-full">
                    <p class="text-md">
                        Lorem ipsum dolor sit amet consectetur adipisicing elit. Quas blanditiis provident officia, nihil quidem similique impedit beatae neque a deserunt minus reiciendis laboriosam libero facere. Hic, molestiae! A, nemo aperiam.
                    </p>
                </div>

                <div class="flex flex-col justify-around gap-4">
                    <a href=""><Button class="w-full">a</Button></a>
                    <a href=""><Button class="w-full">b</Button></a>
                </div>
            </div>
        </div>
    </section>
</template>