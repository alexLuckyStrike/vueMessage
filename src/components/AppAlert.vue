<template>
  <div class="alert danger">
    <p class="alert-title">{{title}}</p>
    <p>{{text}}</p>
    <button class = "btn" :class = "type" v-if = "closable = true" @click="$emit('close')">Закрыть</button>
  </div>
</template>
<script>

export default {
  name: "AppAlert",
  emits:['close'],
  props:{
    text:String,
    title:String,
    closable:{
      type:Boolean,
      default:false,
      required:false
    },
    type:{
      type:String,
      required:false,
      default:'primary',
      validator(val){
        return ['primary','danger','warning'].includes(val)
      }
    }
  }
}

</script>

<style scoped>



</style>