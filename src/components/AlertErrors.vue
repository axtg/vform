<template>
  <div v-if="form.errors.any()" class="message is-danger" role="alert">
    <div class="message-content">
      <div v-if="message" v-html="message"/>

      <ul>
        <li v-for="error in form.errors.flatten()" v-html="error"/>
      </ul>
    </div>
  </div>
</template>

<script>
import Alert from './Alert'

export default {
  name: 'alert-errors',

  extends: Alert,

  props: {
    message: {
      type: String,
      default: 'There were some problems with your input.'
    }
  }
}
</script>
