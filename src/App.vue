<template>
  <div>
    <p v-bind:class="{'active': activeFlag}">我是p标签</p>
        <button @click="activeFlag = !activeFlag">
            Click me
        </button>

         <div class="box" :class="{'active': activeFlag}">
          我是div
        </div>
  </div>
</template>

<script>


export default {
 data() {
  return {
    activeFlag: true
  };
},
  
}
</script>

<style>

</style>
