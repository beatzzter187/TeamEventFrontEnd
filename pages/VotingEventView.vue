<script setup>
</script>
<template>
  <div class="h-full flex justify-center items-center">
    <div class="border h-2/4 w-3/4 flex flex-row">
      <div class="border-2 w-3/4 border-white">
        <div>
          <VoteItem />
          <VoteItem />
          <VoteItem />
        </div>
      </div>
      <div class="border-2 w-1/4 border-white">
        <VoteInput />
        <VoteInput />
        <VoteInput />
      </div>
    </div>
  </div>
</template>
