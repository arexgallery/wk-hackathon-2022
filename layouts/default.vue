<template>
  <main class="min-h-screen flex flex-col">
    <Header />
    <div class="flex-grow flex justify-center">
      <slot />
    </div>
    <Footer />
  </main>
</template>
