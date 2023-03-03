<script setup>
const eventName = ref("");
const Ingredient = ref("");
const datum = ref("");
const zeit = ref("");

const submit = async () => {
  const result = await fetch("http://localhost:4000/api/event/create", {
    headers: {
      "Content-Type": "application/json",
    },
    method: "POST",
    body: JSON.stringify({
      details: {
        creator: "simon",
        date: datum.value.toString(),
        ingredients: [Ingredient.value],
        name: eventName.value,
      },
    }),
  });
  const body = await result.json();
  console.log(body);
};
</script>
<style></style>

<template>
  <div class="text-2xl font-bold ml-5 my-10">
    <h1>Create New Event</h1>
  </div>
  <div class="m-5 font-bold text-xl">
    <label>Event Name</label>
  </div>
  <div class="m-5 w-2/4 h-10">
    <input
      class="w-full h-full placeholder-gray-500 rounded p-4"
      v-model="eventName"
      placeholder="Team Brunch"
    />
  </div>
  <div>
    <div class="m-5 font-bold text-xl">
      <label>Ingredient 1</label>
    </div>
  </div>
  <div>
    <button
      @click="addIngredient"
      class="w-20 h-20 text-2xl font-bold rounded-full bg-slate-600 flex justify-center items-center m-5 content-center"
    >
      +
    </button>
  </div>
  <div class="m-5 flex flex-row">
    <div class="w-1/4 font-bold text-xl">
      <label>Date</label>
    </div>
    <div class="w-1/4 ml-1 font-bold text-xl">
      <label>Time</label>
    </div>
  </div>
  <div class="flex flex-row ml-5">
    <div class="w-1/4 h-10 mr-1">
      <input
        type="Date"
        v-model="datum"
        class="w-full h-full placeholder-gray-500 rounded p-4"
      />
    </div>
    <div class="w-1/4 h-10">
      <input
        type="time"
        class="w-full h-full placeholder-gray-500 rounded p-4"
        v-model="zeit"
      />
    </div>
  </div>
  <div class="w-1/12 m-5 my-10">
    <div
      class="border-2 border-slate-900 rounded font-bold text-xl text-center bg-slate-600 py-2"
    >
      <button>Submit</button>
    </div>
  </div>
</template>
