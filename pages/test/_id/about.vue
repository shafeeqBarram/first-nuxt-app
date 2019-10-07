<template>
  <div>
    Hello World {{$route.params.id}}
  </div>
</template>
<script>
export default{
  head(){
    return{
      title:"This is about page"
    }
  }
}

</script>
