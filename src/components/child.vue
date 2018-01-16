<template lang="pug">
    - var list = [1, 2, 3, 4, 5]
    ul
        each elem in list
            li(@click='clickEvent(' + elem + ')')= elem
</template>

<script>
    export default {
        methods: {
            clickEvent: function(e) {
                console.log(e)
            }
        }
    }
</script>