<script setup lang="ts">
import { ElRadio, ElRadioGroup } from 'element-plus'
import { useWebExtensionStorage } from '~/composables/useWebExtensionStorage'

const theme = useWebExtensionStorage('themeOverride', 'system')
</script>

<template>
  <main class="w-[300px] px-4 py-5 text-center text-gray-700">
    <Logo />
    <h1 class="fw-500 mb-1 color-#5a9cf8" style="font-size: 18px;">
      Theme settings
    </h1>

    <div class="">
      <div class="mb-2 flex items-center text-sm">
        <ElRadioGroup v-model="theme" class="ml-4">
          <ElRadio value="system" size="large">
            Automatic (follow OS setting)
          </ElRadio>
          <ElRadio value="force_dark" size="large">
            Force dark theme
          </ElRadio>
          <ElRadio value="force_light" size="large">
            Force light theme
          </ElRadio>
        </ElRadioGroup>
      </div>
    </div>
  </main>
</template>
