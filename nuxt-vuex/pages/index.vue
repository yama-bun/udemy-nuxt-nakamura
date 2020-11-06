<template>
  <div>
    <h1>
      {{ $store.state.hello.message }}
    </h1>
    <button v-on:click="$store.dispatch('hello/updateMessageAction', 'Dispatch with payload')">Dispatch</button>
  </div>
</template>

<script>
export default {}
</script>

