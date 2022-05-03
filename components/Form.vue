<template>
    <div class="flex flex-col justify-center items-center rounded-lg bg-cyan-300 w-fit">
        <input class="m-2 pl-3 py-2 outline-0 text-lime-600 text-3xl bg-emerald-200 border-2 border-lime-600 rounded" placeholder="Your name" type="text" name="Name" id="name" v-model="custName" @keyup="updateLabel" />
        <button class="m-2 rounded outline-0 text-3xl bg-lime-600 text-emerald-200 p-3" @click.prevent="submit">Submit</button>
    </div>
</template>

<script lang="ts">


export default {
  name: 'Form',
  data:()=>{
      return {
          custName:''
      }
  },
  methods:{
      submit(){
          this.updateLabel()
          this.custName=''
      },
      updateLabel(){
          this.$emit('name-fetch',this.custName)
      }
  },
}
</script>