<template>
  <div>
      <!-- <div>
    <h1>{{count}}  </h1> 
    <button class="btn btn-primary" v-on:click="increment">Increment</button>
    <button class="btn btn-success" v-on:click="decrement">Decrement</button>


  </div> -->
      <form @submit.prevent>
    <div class="  w-75 mx-auto">
 
<div class="mb-3">
  <label for="exampleFormControlInput1" class="form-label">Name</label>
  <input  v-model="comment.name"  type="text"   class="form-control" id="exampleFormControlInput1" placeholder="Name">
</div>
 <div class="mb-3">
  <label for="exampleFormControlInput1" class="form-label">Email  </label>
  <input type="email" v-model="comment.email"    class="form-control" id="exampleFormControlInput1" placeholder="Email">
</div>
<div class="mb-3">
  <label for="exampleFormControlInput1" class="form-label">Content</label>
  <input type="text"  v-model="comment.content"   class="form-control" id="exampleFormControlInput1" placeholder="Content">
</div>
      <button @click="createComment" class="btn   btn-primary">Add comments</button>
</div>
  </form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      comment:{
      name:"",
      email:"",
      content:""  
      }
 
    }
  },
      methods: {
      createComment(){
        this.comment.id = Date.now();
        this.$emit('addComment', this.comment)
        this.comment ={
        name:"",
        email:"",
        content:""  
      }
      }
    },
}
</script>
<style >
  
</style>