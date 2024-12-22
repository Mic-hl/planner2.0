<script setup>
import AuthenticatedLayout from '@/Layouts/AuthenticatedLayout.vue';
import Recipe from '../Components/Recipe.vue';
import { Head } from '@inertiajs/vue3';
</script>

<template>
    <Head title="Recipes" />

    <AuthenticatedLayout>
        <template #header>
            <h2>Recipes</h2>
        </template>

        <div class="content-wrapper">
            <ul class="recipe-list">
                <!-- @foreach -->
                <li>
                    <Recipe
                        title="Spaghetti Carbonara"
                        :ingredients="['Spaghetti', 'Eggs', 'Parmesan', 'Bacon', 'Black Pepper']"
                        preparation="Boil spaghetti. Cook bacon. Mix eggs with parmesan and combine with cooked spaghetti and bacon."
                        difficulty="Medium"
                        :time="30"
                    />
                </li>
                <!-- @endforeach -->
            </ul>
        </div>
    </AuthenticatedLayout>
</template>

<script>
    export default {
        components: {
            Recipe,
        },
    };
</script>