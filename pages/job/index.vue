<template>
  <main class="grid grid-flow-row gap-8">
    <!-- Header -->
    <div class="flex items-center justify-between">
      <h1 class="text-[#0A0A0A] font-medium text-lg">Job Desk</h1>
      <div class="flex items-center space-x-4 text-sm">
        <button class="bg-[#212143] text-[#f5f5f5] rounded-md px-4 py-2 font-medium">
          <Icon name="material-symbols:add" size="1.3em" />
          Action
        </button>
      </div>
    </div>
    <!-- Header -->
    <!-- Main Section  -->
    <section>
      <div>
        Yello
      </div>
      <div>
        Yello
      </div>
    </section>
    <!-- Main Section  -->
    
  </main>
</template>

<style lang="scss" scoped>
section {
    grid-template-columns: 250px 1fr;
    @apply gap-6 grid;
    div {
      @apply bg-red-50;
    }
}
</style>