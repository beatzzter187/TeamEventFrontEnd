<script setup>

const events = ref([])

onMounted(async () => {
    const data = await fetch("http://localhost:4000/api/event/events")
    events.value = await data.json()
    console.log(events.value)
})

</script>

<template>
    <div class="flex justify-center p-32">
        <div class="border-2 border-l-rose-400 p-3 w-full" v-for="el in events" :key="el.id">
            <EventItem :event="el" />
        </div>
    </div>
</template>