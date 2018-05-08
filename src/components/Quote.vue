<template>
   <div class="col-sm-6 col-md-4 col-lg-3">
       <div class="panel panel-defaut">
           <div class="panel-body quote">
               <slot></slot>
           </div>
       </div>

   </div>
</template>

<script>
    export default {
        props: ["quotes"],
        
    }
</script>

<style>
 .panel-body{
     font-family: "Arizonia", cursive;
     font-size: 24px;
     color: #666;
 }
 .quote {
     cursor: pointer;
 }
.quote:hover {
     background: lightcoral;
 }
</style>
