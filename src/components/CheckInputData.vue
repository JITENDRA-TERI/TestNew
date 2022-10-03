<template>
    <div>
         <input type="text" placeholder="Test"  v-model="testname" />
         <input type="text" placeholder="first name"  v-model="firstname" />
         <input type="text" placeholder="last name"  v-model="lastname" />
    </div>
</template>

<script>
    import { ref, reactive, toRefs} from 'vue'

    export default {
        name:"CheckInputData",
        setup()
        {
            const testname= ref('')
            const state = reactive({
                firstname:'',
                lastname:''
            })

            return{
                testname,
                ...toRefs(state)
            }
        }
        
    }
</script>

<style scoped>

</style>