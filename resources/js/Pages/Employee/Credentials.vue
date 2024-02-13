<script setup>
import AppLayout from '@/Layouts/AppLayout.vue';
import TextInput from '@/Components/TextInput.vue';
import InputLabel from '@/Components/InputLabel.vue';
import { Head } from '@inertiajs/vue3';

const props = defineProps({
    credentials: Object
})
</script>

<template>
    <Head title="Success!" />

    <AppLayout>
        <div class="py-12">
            <div class="w-full px-12">
                <h1 class="text-2xl text-gray-700 font-bold mb-9">Default Login Credentials</h1>
                <!-- <p class="text-sm text-gray-500 mb-4">{{ props.credentials.username }}  {{ props.credentials.password }}</p> -->

                <div class="max-w-4xl w-full">
                        <div class="flex items-start space-x-3 mb-4">
                            <InputLabel for="username" value="Username" class="shrink-0 w-[150px]" />

                            <div class="block w-full">
                                <TextInput
                                id="username"
                                v-model="props.credentials.username"
                                type="text"
                                maxlength="6"
                                class="w-full"
                                readonly
                                />

                            </div>
                        </div>

                     <div class="max-w-4xl w-full">
                        <div class="flex items-start space-x-3 mb-4">
                            <InputLabel for="password" value="Password." class="shrink-0 w-[150px]" />

                            <div class="block w-full">
                                <TextInput
                                id="password"
                                v-model="props.credentials.password"
                                type="text"
                                maxlength="6"
                                class="w-full"
                                readonly
                                />
                            </div>
                        </div>
                  </div>
            </div>
        </div>
     </div>
    </AppLayout>
</template>
