<template>
  <div />
</template>

<script lang="ts">
import Vue from 'vue'
import { Component } from 'vue-property-decorator'
import { navigate } from '@/utils'

@Component({})
export default class Signin extends Vue {
  /** Called when component is created. */
  protected created () {
    // navigate to BC Registry login page then return to this app
    const loginUrl = sessionStorage.getItem('REGISTRY_HOME_URL') + 'login'
    const returnUrl = encodeURIComponent(sessionStorage.getItem('BASE_URL'))
    navigate(`${loginUrl}?return=${returnUrl}`)
  }
}
</script>
