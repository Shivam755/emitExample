<template>
    <div class="h-screen flex flex-col justify-center items-center bg-rose-100" >
        <h1 class="text-5xl text-purple-700 m-4">Hello {{cName}}</h1>
        <Form @name-fetch='greet' />
    </div>
</template>

<script lang="ts">
import Form from '@/components/Form.vue'

export default {
  name: 'IndexPage',
  components:{
      Form
  },
  data(){
      return{
          cName:''
      }
  },
  methods:{
      greet(e){
          console.log(e)
          this.cName=e
      },
  },
}
</script>