<template>
  <div>
    <header class="shadow-sm bg-stone-950">
      <nav class="container mx-auto p-4">
        <NuxtLink to="/products" class="font-bold">Void products</NuxtLink>
      </nav>
    </header>

    <div class="container mx-auto p-4 text-black">
      <slot />
    </div>

    <footer class="container mx-auto p-4 flex justify-between border-t-2">
      <ul class="flex gap-4">
        <li><NuxtLink to="/">Home</NuxtLink></li>
        <li><NuxtLink to="/about">About</NuxtLink></li>
        <li><NuxtLink to="/products">Products</NuxtLink></li>
      </ul>
    </footer>
  </div>
</template>

<style scoped>
.router-link-exact-active {
  color: #8a2be2;
}
</style>
