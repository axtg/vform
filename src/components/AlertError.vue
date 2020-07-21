<template>
  <div v-if="form.errors.any()" class="message is-danger" role="alert">
    <slot>
      <div class="message-body">
        <div v-if="form.errors.has('error')" v-html="form.errors.get('error')"/>
        <div v-else v-html="message"/>
      </div>
    </slot>
  </div>
</template>

<script>
import Alert from './Alert'

export default {
  name: 'alert-error',

  extends: Alert,

  props: {
    message: {
      type: String,
      default: 'There were some problems with your input.'
    }
  }
}
</script>
