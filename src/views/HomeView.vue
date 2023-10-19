<script setup lang="ts">
import { defineAsyncComponent } from 'vue';

const SVGCloud = defineAsyncComponent(() => import("@/components/icons/SVGCloud.vue"))
const SVGCloudSync = defineAsyncComponent(() => import("@/components/icons/SVGCloudSync.vue"))
const SVGStorage = defineAsyncComponent(() => import("@/components/icons/SVGStorage.vue"))
const SVGArrowRight = defineAsyncComponent(() => import("@/components/icons/SVGArrowRight.vue"))
const SVGArrowDown = defineAsyncComponent(() => import("@/components/icons/SVGArrowDown.vue"))
</script>

<template>
  <div class="grid grid-cols-1 md:grid-cols-5 h-screen">
    <div class="filter invert md:col-span-2 flex items-center justify-center h-full p-8 md:p-0">
      <div class="w-40 md:max-w-xs">
        <img src="/logo.png" alt="Logo">
      </div>
    </div>
    <div class="md:col-span-3 flex flex-col justify-center text-box p-8 md:p-0">
      <p class="text-lg text-center py-4">Simple cloud based file storage solutions</p>
      <div class="flex flex-col md:flex-row items-center gap-x-4 justify-center my-5">
        <div class="md:w-[13ch] flex flex-col items-center justify-center text-center gap-y-2">
          <SVGStorage />
          <p class="text-sm">Protect files on your device</p>
        </div>
        <SVGArrowRight class="hidden md:block" />
        <SVGArrowDown class="block md:hidden" />
        <div class="md:w-[13ch] flex flex-col items-center justify-center text-center gap-y-2">
          <SVGCloudSync />
          <p class="text-sm">Sync files in real time</p>
        </div>
        <SVGArrowRight class="hidden md:block" />
        <SVGArrowDown class="block md:hidden" />
        <div class="md:w-[13ch] flex flex-col items-center justify-center text-center gap-y-2">
          <SVGCloud />
          <p class="text-sm">Secure files safely on the cloud</p>
        </div>
      </div>
      <div class="mx-auto text-center">
        <button class="border border-white px-4 py-2 hover:bg-white hover:text-black">
          Get the App
        </button>
      </div>
    </div>
  </div>
</template>

<style scoped>
.text-box{
  background: rgb(0,0,0);
background: -moz-linear-gradient(31deg, rgba(0,0,0,0.8799894957983193) 0%, rgba(4,5,14,1) 75%, rgba(4,31,163,0.8855917366946778) 97%);
background: -webkit-linear-gradient(31deg, rgba(0,0,0,0.8799894957983193) 0%, rgba(4,5,14,1) 75%, rgba(4,31,163,0.8855917366946778) 97%);
background: linear-gradient(31deg, rgba(0,0,0,0.8799894957983193) 0%, rgba(4,5,14,1) 75%, rgba(4,31,163,0.8855917366946778) 97%);
filter: progid:DXImageTransform.Microsoft.gradient(startColorstr="#000000",endColorstr="#041fa3",GradientType=1);
}
</style>
