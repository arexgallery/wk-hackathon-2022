<template>
  <div class="py-20 px-10 text-center">
    <Head>
      <Title>Home</Title>
    </Head>
    <Logos class="mb-6" />
    <Suspense>
      <PageView />
      <template #fallback>
        <div class="opacity-50 italic">
          <span class="pulse">Loading...</span>
        </div>
      </template>
    </Suspense>
    <InputEntry />
    <div class="flex justify-center">
      <div class="m-4">
        <BaseCard>
          <h3>Retro</h3>
        </BaseCard>
      </div>
      <div class="m-4">
        <BaseCard>
          <h3>SprintPlanning</h3>
        </BaseCard>
      </div>
    </div>
  </div>
</template>
