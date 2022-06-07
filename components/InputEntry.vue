<script setup lang="ts">
interface Props {
  placeholder: string
  handleSubmit: (team: string) => void
}
const props = withDefaults(defineProps<Props>(), {
  placeholder: '',
  handleSubmit: () => {},
})

const name = ref('')
</script>

<template>
  <div class="max-w-xs space-y-4 mx-auto mt-4">
    <BaseInput
      id="input"
      v-model="name"
      class="text-center"
      :placeholder="placeholder"
      type="text"
      autocomplete="false"
      @keydown.enter="() => handleSubmit(name)"
    />
    <div>
      <BaseButton
        class="disabled:cursor-not-allowed"
        :disabled="!name"
        @click="() => handleSubmit(name)"
      >
        GO
      </BaseButton>
    </div>
  </div>
</template>
