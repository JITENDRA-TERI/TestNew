<template>
    <div>
       <h2>{{count}}</h2>
       <button @click="Incrementcount">Click On button</button>

       <h2>{{firstname}} {{lastname}}</h2>
       <button @click="Changename">Change Name</button>
    </div>
</template>

<script>

import { reactive, ref, toRefs } from 'vue'

    export default {
        name: 'CheckMethod',
         setup()
        {
            const count=ref(0)
            const state= reactive({
                firstname: 'Testfirstname',
                lastname: 'testlastname'
            })
            function Incrementcount()
            {
                count.value++
            }

            function Changename()
            {
                state.firstname ='Changefirst',
                state.lastname ='Changelast'
            }

            return {
                   count,
                   Incrementcount,
                   ...toRefs(state),
                   Changename
            }
        },
        
    }
</script>

<style scoped>

</style>