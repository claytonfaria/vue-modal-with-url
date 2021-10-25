<template>
  <div class="fixed inset-0 flex items-center justify-center">
    <input v-model="nome" type="text" class="px-2 text-black" @keydown.enter="go">
    <button
      class="px-4 py-2 text-sm font-medium text-white bg-black rounded-md bg-opacity-20 hover:bg-opacity-30 focus:outline-none focus-visible:ring-2 focus-visible:ring-white focus-visible:ring-opacity-75"
      @click="go"
    >
      Check user details
    </button>
  </div>
</template>
<script setup lang="ts">
const nome = ref('')
const router = useRouter()

const go = () => {
  router.push(`/contacts/${nome.value}`)
}

</script>
