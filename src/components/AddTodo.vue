<template>
    <div>
        <form>
            <input type="text" v-model="title" name="title" placeholder="Add to do..."/>
            <input type="text" v-model="title2" name="title" placeholder="Add to do 2..."/>
            <input type="submit" value="submit" class="btn"/>
        </form>
    </div>
</template>
<script>
export default {
  name: "AddTodo",
  data(){
      return{
          title:''
      }
  }  
}
</script>
<style scoped>
form{
    display: flex;
}
input[type="text"]{
    flex: 10;
    padding: 5px;
}
input[type="submit"]{
    flex:2;
}
</style>