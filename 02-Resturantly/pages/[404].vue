<template>
  <div>
    <div class="container">
      <NuxtLayout name="error">
        <template #header>
          <h1>Page was not found 404</h1>
        </template>

        <template #redirectEl>
          <a href="/restaurants">
            Go Back
          </a>
        </template>
      </NuxtLayout>
    </div>
  </div>
</template>

<style scoped>
  .container {
    text-align: center;
    margin-top: 5rem;
  }
</style>