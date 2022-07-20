<template>
  <div class="py-20 px-10 text-center">
    <Suspense>
      <QueryBible />
      <template #fallback>
        <div class="opacity-50 italic">
          <span class="pulse">Loading...</span>
        </div>
      </template>
    </Suspense>
  </div>
</template>
