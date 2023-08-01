
<script setup>

import {ref} from "vue";

const showImage=ref(true);

</script>



<template>
  <section class="mx-auto container">
    <h1>----------------------------------------------------------</h1>
    <h1 class="text-2xl mb-10">Checkbox</h1>
    <p class="mb-10">{{ showImage }}</p>
    <label for="">Display Random Image</label>
    <input class="ml-2" type="checkbox" v-model="showImage"  />
    <p class="mt-5">
      <input type="radio" name="display" :value="true" v-model="showImage" > On <br/>
      <input type="radio" name="display" :value="false" v-model="showImage"> Off <br/>
    </p>
    <img v-show="showImage"
        class="mt-10 mx-auto w-[500px]"
        :src="`https://source.unsplash.com/random`"
        alt=""  />

    <!-- <img
    v-if="displayImage"
    class="mt-10 mx-auto w-[500px]"
    :src="`https://source.unsplash.com/random?version=${Math.random()}`"
    alt=""  /> -->

  </section>
</template>



<style scoped>

</style>