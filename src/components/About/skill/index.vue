<template lang="pug">
    label.skill
        .skill-name {{ title }}
        .input-wrap
            input(type="text" :value="percents" maxlenght="3").skill-input.input
            .skill-measure %
        .remove-btn
            button(type="button" @click="emitRemote") -
</template>

<script>
export default {
  props: {
    title: {
        type: String,
        default: 'Html'
    },
    id :{
       type: Number 
    },
    percents: {
        type: Number,
        default: 100
    }
  },
  methods: {
      emitRemove(){
          this.$emit('removeSkill', this.id)
      }
  }
}
</script>
<style src="./style.scss" lang="scss" scoped></style>

