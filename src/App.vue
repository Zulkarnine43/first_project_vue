<template>
<div>
  <div>
  <button @click="ComponentToRender='CompHeader' ">Header</button>
  <button @click="ComponentToRender='CompForm' ">Form</button>
  <button @click="ComponentToRender='CompFooter' ">Footer</button>
  </div>
  <CompHeader
  :firstName="fName"
  :lastName="lName"
  :age="myAge"
  @updateValue="fName =$event"
  />
  <CompFooter>
    <ul>
      <li>HTML</li>
       <li>CSS</li>
        <li>PHP</li>
    </ul>
  </CompFooter>
  <CompForm></CompForm>
 
</div>
</template>

<script>
import CompHeader from './components/header_footer/header.vue';
import CompFooter from './components/header_footer/footer.vue';
import CompForm from './components/header_footer/form.vue';
export default {
data(){
 return{
   fName:"Zulkar",
   lName:"Nine",
   myAge:21,
   ComponentToRender:'CompHeader'
 }
},
components:{
  CompHeader,
  CompFooter,
  CompForm
}
}
</script>

<style>
 body{
   font-family: 'Viaoda Libre', cursive;
 }
</style>
