<template>
    <div>
          <h3>Name: {{ o_firstname }}</h3>
          <h3>Composition Name: {{ c_firstname }}</h3>
          <h3>Greet Name : {{greet}}</h3>

          <h2>{{ state.firstname }}   {{ state.lastname }}</h2>
    </div>
</template>

<script>
import { ref, reactive } from 'vue'
    export default {
        name:'DataNews',
        setup()
        {
            const c_firstname =ref('test2')
            const greet = `Hello  ${c_firstname.value}`

           const  state = reactive({
                firstname: 'newtestname',
                lastname: 'testlastname'
            })

            const reactiveGreet= `hello ${ state.firstname }  ${ state.lastname }`
            
            return{
                c_firstname,
                greet,
                state,
                reactiveGreet,

            }
        },
       
    }
</script>

<style scoped>

</style>