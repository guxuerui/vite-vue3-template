<script setup lang="ts">
const router = useRouter()
const jumpPage = (folder: string, name: string) => {
  if (folder && name)
    router.push(`/${folder}/${encodeURIComponent(name)}`)
}
</script>

<template>
  <div flex="~ gap2" justify-start p4>
    <button btn @click="jumpPage('example', 'test')">
      Go to a vue file
    </button>
    <button btn @click="jumpPage('example', 'test1')">
      Go to a markdown file
    </button>
  </div>
</template>

<style scoped>
</style>
