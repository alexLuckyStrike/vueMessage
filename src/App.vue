<template>
  <div class="container">
    <AppAlert
        v-if="alert"
        text = "Это очень важное сообщение, будьте бдительны!"
        title = "Внимание"
        type = "danger"
        :closable = "true"
        @close = "alert = false"
    >
    </AppAlert>

    <div class="card">
        <button class="btn primary" @click = "toggleAlert"> {{ alert ? 'Скрыть' : 'Показать' }} Показать сообщение</button>
    </div>

    <app-block></app-block>
  </div>
</template>
<script>

import AppAlert from "./components/AppAlert";
import AppBlock from "./components/AppBlock";


export default {
  components:{AppBlock, AppAlert }
}

</script>

