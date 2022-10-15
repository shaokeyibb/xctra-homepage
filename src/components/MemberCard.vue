<template>
  <div style="display:flex; flex-direction: row; align-items: center">
    <img
        :src="avatar"
        style="margin: 10px; border-radius: 100%; width: 50px; height: 50px"
        alt="avatar"/>
    <div>
      <span>{{ name }}</span>
      <template v-if="githubId && githubId !== ''">
        （<a :href="`https://github.com/${githubId}`" target="_blank">@{{ githubId }}</a>）
      </template>
      <template v-if="description && description !== ''">
        <span style="color: var(--el-text-color-secondary); margin-left: 5px;"> —— {{ description }}</span>
      </template>
      <template v-if="isSpecial">
        <span style="color: var(--el-color-primary); margin-left: 10px">特邀嘉宾</span>
      </template>
    </div>
  </div>
</template>

<script setup>
import md5 from 'js-md5'
import {computed} from "vue";

const props = defineProps({
  name: {
    type: String,
    required: true
  },
  email: {
    type: String,
    required: false,
    default: ""
  },
  description: {
    type: String,
    required: false,
    default: ""
  },
  isSpecial: {
    type: Boolean,
    required: false,
    default: false
  },
  githubId: {
    type: String,
    required: false,
    default: ""
  }
})

const avatar = computed(() => {
  return `https://cravatar.cn/avatar/` + md5.hex(props.email.trim().toLowerCase())
})
</script>

<style scoped>

</style>
