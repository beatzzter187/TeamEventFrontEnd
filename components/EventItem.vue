<script setup>

defineProps(["event"])
</script>

<template>
    <h3>{{ event.name }} >>>>>>>> {{ event.date }} >>>>>>>>> {{ event.ingredients.toString() }}</h3>
</template>
