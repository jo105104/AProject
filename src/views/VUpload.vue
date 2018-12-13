<template>
  <div class="VideoUploadArea">
    <videoupload />
  </div>
</template>

<script>
// @ is an alias to /src
  import videoupload from '@/components/VideoUpload.vue'

  export default {
    name: 'upload',
    components: {
      videoupload
    }
  }
</script>