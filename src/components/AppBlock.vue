<template>
  <div class="container">
    <AppAlert
        v-if="alert"
        text = "Это очень важное сообщение, будьте бдительны!"
        title = "Внимание!"
        @close = "alert = false"
    >
    </AppAlert>

    <div class="card">
      <button class="btn primary" @click = "toggleAlert"> {{ alert ? 'Скрыть' : 'Показать' }} Показать сообщение</button>
    </div>

  </div>
</template>

<script>
import AppAlert from "./AppAlert";


export default {
components:{AppAlert}

}
</script>

<style scoped>

</style>