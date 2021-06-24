<template>
 <div>
     <!-- <ul>
         <li v-for="stu in myStudents" :key="stu">
             {{stu}}
         </li>
     </ul> -->
     <p>firstName: {{firstName}}</p>
     <p>LastName: {{lastName}}</p>
     <p>Age: {{age}}</p>
     <button @click="updateName">Click Me</button>
     </div>   
</template>

<script>


export default {
 props:{
    firstName: String,
    lastName: String,
    age: Number
 },
 methods:{
     updateName(){
        //  this.firstName="Abul"
        this.$emit('updateValue','Abul');
     }
 }
}
</script>

<style scoped>
div{
  color: red;
}
</style>>
