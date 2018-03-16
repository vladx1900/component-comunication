<template>
  <div class="container">
    <div class="row text-center">
      <div class="col-xs-12">
          <app-parent></app-parent>
      </div>
    </div>
  </div>
</template>

<script>
import Parent from './components/Parent.vue';

export default {
  name: 'App',
  components: {
    appParent: Parent
  }
}
</script>

<style>

</style>
