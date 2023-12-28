<template>
  <section
    class="container-10x border-all dim-white-border mx-auto flex flex-col items-stretch gap-5 rounded-2xl py-10"
  >
    <div class="flex w-full justify-between gap-2">
      <Button :icon="caseIcon" text="case" />
      <Button :icon="checkIcon" />
      <Button :icon="deleteIcon" text="clear" @click="clearText" />
      <Button :icon="copyIcon" text="copy" />
      <Button :icon="cutIcon" text="cut" />
      <Button :icon="pasteIcon" text="paste" />
      <Button :icon="selectAllIcon" @click="selectAllText" />
      <Button :icon="undoIcon" text="undo" />
      <Button :icon="redoIcon" text="redo" />
      <Button :icon="saveIcon" text="save" />
    </div>
    <textarea
      ref="textarea"
      cols="30"
      rows="10"
      v-model="text"
      class="border-all dim-white-border gradient rounded-lg p-10 text-white text-opacity-70 outline-none focus:border-opacity-50"
      placeholder="Write something here ..."
    ></textarea>
  </section>
</template>

<script setup>
// import { ref } from 'vue'
import caseIcon from '~/assets/images/case-icon.svg'
import checkIcon from '~/assets/images/check-icon.svg'
import deleteIcon from '~/assets/images/delete-icon.svg'
import copyIcon from '~/assets/images/copy-icon.svg'
import pasteIcon from '~/assets/images/paste-icon.svg'
import cutIcon from '~/assets/images/cut-icon.svg'
import selectAllIcon from '~/assets/images/select-all-icon.svg'
import undoIcon from '~/assets/images/undo-icon.svg'
import redoIcon from '~/assets/images/redo-icon.svg'
import saveIcon from '~/assets/images/save-icon.svg'

const text = ref('')
const textarea = ref(null)

const clearText = () => {
  text.value = ''
}

const selectAllText = () => {
  textarea.value.select()
}
</script>
