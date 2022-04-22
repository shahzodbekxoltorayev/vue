<template>
  <!-- <div>
    <h1>{{count}}  </h1> 
    <button class="btn btn-primary" v-on:click="increment">Increment</button>
    <button class="btn btn-success" v-on:click="decrement">Decrement</button>


  </div> -->
  <form @submit.prevent>
    <div class="  w-75 mx-auto">
 
<div class="mb-3">
  <label for="exampleFormControlInput1" class="form-label">Name</label>
  <input @input="name=$event.target.value" type="text"  :value="name" class="form-control" id="exampleFormControlInput1" placeholder="Name">
</div>
 <div class="mb-3">
  <label for="exampleFormControlInput1" class="form-label">Email  </label>
  <input type="email" @input="email=$event.target.value"  :value="email" class="form-control" id="exampleFormControlInput1" placeholder="Email">
</div>
<div class="mb-3">
  <label for="exampleFormControlInput1" class="form-label">Content</label>
  <input type="text"  @input="content=$event.target.value" :value="content" class="form-control" id="exampleFormControlInput1" placeholder="Content">
</div>
      <button @click="createComment" class="btn   btn-primary">Add comments</button>
</div>
  </form>
 
  <div class="comment w-75 mx-auto" v-for="comment in comments" v-bind:key="comment.id">
    <div><b>Name:</b> {{comment.name}}</div>
    <div><b>Email:</b> {{comment.email}}</div>
    <div><b>Content:</b > {{comment.content}}</div> 
  </div>
</template>

<script>
export default {
  data() {
    return {
     comments:[
       {
         id:1,
         name:"Samar",
         email:"samar@gmail.com",
         content:"Lorem ipsum, dolor sit amet consectetur adipisicing. "  
       },
              {
         id:1,
         name:"Samar",
         email:"samar@gmail.com",
         content:"Lorem ipsum, dolor sit amet consectetur adipisicing. "  
       },
              {
         id:1,
         name:"Samar",
         email:"samar@gmail.com",
         content:"Lorem ipsum, dolor sit amet consectetur adipisicing. "  
       },
              {
         id:1,
         name:"Samar",
         email:"samar@gmail.com",
         content:"Lorem ipsum, dolor sit amet consectetur adipisicing. "  
       },
     ],
     name:"",
     email:"",
     content:"" 
    }
  },
  methods: {
    // increment(){
    //   this.count +=1
    // },
    // decrement(){
    //   this.count -=1
    // },
    createComment(){
      const newComment = {
          id:Date.now(),
          name:this.name,
          email:this.email,
          content:this.content
      }
      this.comments.push(newComment)
      this.name=""
      this.email=""
      this.content=""
    }
  },
}
</script>

<style  >
.comment{
  border: 1px solid #ccc;
  padding: 10px;
  margin: 10px;
}
</style>