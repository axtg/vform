<template>
  <div v-if="form.successful" class="message is-success" role="alert">
    <slot>
      <div class="message-content" v-html="message"/>
    </slot>
  </div>
</template>

<script>
import Alert from './Alert'

export default {
  name: 'alert-success',

  extends: Alert,

  props: {
    message: { type: String, default: '' }
  }
}
</script>
