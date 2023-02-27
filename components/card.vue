<script setup>
const props = defineProps({
  card: Object
})
</script>

<template>
  <div
    class="brutal ring-2 ring-black border-1 border-l-6 border-t-6 border-solid border-white w-80 h-120 bg-slate-200 flex flex-col justify-center items-center">
    <div class="text-4xl flex-grow flex items-center">
      <div>{{ props.card.tr }}</div>
    </div>
    <div class="p-2">{{ props.card.en }}</div>
  </div>
</template>

<style>
.brutal {
  font-family: ViolentSans;
  font-weight: 600;
}

.brutal:after {
  content: '';
  position: absolute;
  background-color: black;
  top: 8px;
  left: 8px;
  right: -8px;
  bottom: -8px;
  z-index: -1;
}
</style>