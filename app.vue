<template>
  <div class="flex flex-col min-h-screen">
    <TheNavbar />
    <main class="flex-1">
      <NuxtPage />
    </main>
    <TheFooter />
  </div>
</template>

<style scoped lang="scss">
@use "~/assets/scss/_variables.scss" as *;

main {
  background-color: $secondaryColor;
  color: $primaryColor;
}
</style>
