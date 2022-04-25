<template>
 
 <comment-form @addComment ="createComment"></comment-form>
   <comment-list :comments="comments"></comment-list>
 
 
</template>

<script>
import CommentForm from './components/CommentForm';
import CommentList from './components/CommentList'
export default {
  components:{
    CommentForm,
    CommentList
  },
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
    createComment(comments){
      this.comments.push(comments)
    }
  },
}
</script>

<style  >
 
</style>