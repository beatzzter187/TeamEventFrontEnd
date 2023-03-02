<template>
  <div class="flex h-screen">
    <nav class="bg-slate-700 w-1/4">
      <div class="mx-20 my-10 m-5 flex">
        <NuxtLink
          to="/CreateEventView"
          class="bg-lime-300 rounded grow text-center py-5"
        >
          A
        </NuxtLink>
      </div>
      <div class="flex mx-20 m-5 my-10">
        <NuxtLink
          to="/VotingEventView"
          class="bg-lime-300 rounded grow text-center py-5"
          >B</NuxtLink
        >
      </div>
      <div class="flex mx-20 m-5 my-10">
        <NuxtLink to="/AllEventsView" class="bg-lime-300 rounded grow text-center py-5">C</NuxtLink>
      </div>
    </nav>
    <div class="bg-slate-500 grow content-center">
      <NuxtPage />
    </div>
  </div>
</template>
