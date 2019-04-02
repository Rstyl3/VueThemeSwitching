<template>
  <main>
    <h1>my awesome portfolio</h1>
    <div class="grid">
      <div class="item">
        <h1>project a</h1>
        <button>learn more</button>
      </div>
      <div class="item">
        <h1>project b</h1>
        <button>learn more</button>
      </div>
      <div class="item">
        <h1>project c</h1>
        <button>learn more</button>
      </div>
      <div class="item featured">
        <h1>project d</h1>
        <button>learn more</button>
      </div>
    </div>
  </main>
</template>

<script>
export default {

}
</script>

<style scoped>
.item {
  background: var(--secondary-background);
}
button {
  background: var(--primary);
  color: var(--secondary-background);
}
</style>
