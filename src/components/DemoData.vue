<template>
    <div>
      <h3>{{ usernames }}</h3>
    </div>
</template>

<script>
import { ref } from 'vue'
    export default {
        name: 'DemoData',
        setup() {
           const usernames = ref('Newfile')

           setTimeout(() => {
             usernames.value="testnameview"
            
           }, 20000 )

           return{
            usernames
        }
        }
        
    }
</script>

<style scoped>

</style>