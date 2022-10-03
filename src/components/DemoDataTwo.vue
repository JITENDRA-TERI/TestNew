<template>
    <div>
          <h3>{{ firstname }} {{ lastname }}</h3>
    </div>
</template>

<script>
import { reactive, toRefs } from 'vue'
    export default {
        setup()
        {
         const state = reactive({
                firstname:'firstnames',
                lastname:'lastnames'

            })
            setTimeout(() => {
              state.firstname = "Firstnames new",
              state.lastname = "lastnames new"
            
           }, 20000 )

            return toRefs(state)

        }
    }
</script>

<style scoped>

</style>