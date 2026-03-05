<script setup>
import Layout from './components/layouts/Layout.vue';
import Dashboard from './components/pages/Dashboard.vue';
import Welcome from './components/pages/Welcome.vue';
import Workout from './components/pages/Workout.vue';

const selectedDisplay = 3;


</script>

<template>
  <Layout>
    <Welcome v-if="selectedDisplay == 1" />
    <Dashboard v-if="selectedDisplay == 2" />
    <Workout v-if="selectedDisplay == 3" />
  </Layout>
</template>

<style scoped>
  #welcome,
    .challenge,
    .benefits {
        display: flex;
        flex-direction: column;
    }

    #welcome {
        gap: 1.5rem;
    }

    .benefits {
        gap: 0.5rem;
    }

    .challenge {
        gap: 0.25rem;
    }

    @media (min-width: 640px) {
        #welcome {
            gap: 2rem;
            padding: 1rem 0;
        }

        .benefits {
            gap: 1rem;
        }
    }
</style>
