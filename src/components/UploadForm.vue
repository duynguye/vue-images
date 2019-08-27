<template>
  <div class="dropper">
    <input 
      type="file" 
      @change="uploadImages($event.target.files)"
      multiple
      accept="image/*"
    />

    <span>Drag files here!</span>
  </div>
</template>

<script>
import { mapActions } from 'vuex'

export default {
  name: 'UploadForm',
  methods: mapActions(['uploadImages'])
}
</script>

<style scoped>
.dropper {
  align-items: center;
  border: 2px dashed black;
  border-radius: 5px;
  cursor: pointer;
  display: flex;
  height: 30vh;
  justify-content: center;
}

.dropper:hover {
  background-color: #eee;
}

input {
  height: 30vh;
  position: absolute;
  opacity: 0;
  width: 100%;
}
</style>