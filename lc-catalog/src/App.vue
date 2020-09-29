<template>
  <div id="app">
    <header>
      <NavBar/>
      <BookTable/>
    </header>
  </div>
</template>

<script>
import NavBar from "@/components/NavBar";
import BookTable from "@/components/BookTable";


export default {
  name: 'App',
  components: {
    NavBar,
    BookTable
  }
}
</script>

<style lang="scss">
@import "~bulma/css/bulma.css";
#button {

}
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: 'montserrat', sans-serif;
}

header {
  width: 100vw;
  background-color: purple;
  padding: 25px;
}
</style>
