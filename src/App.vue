<template lang="pug">
  div(class='hello') nyan
    // html is cached so need to change when reflesh
    //- this comment is erased after conversion
    - var random = Math.round(Math.random()*3)
    case random
      when 0
        div 0
      when 1
        div 1
      default
        div above 2
    h1 {{hoge}}
    child
</template>

<script>
import child from './components/child'

export default {
  name: 'App',
  data() {
    return {
      hoge: 22
    }
  },
  components: {
    child
  }
}
</script>