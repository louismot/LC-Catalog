<template>
  <h2 class="title is-2" style="color: yellow">Ms. Criden's Lucy Calkins Catalog</h2>
  <nav>
    <div class="menu-item">
      <a href="#">
        Students
      </a>
    </div>
    <div class="menu-item" >
      <a href="#" @click="isTeacher">
        Teacher
      </a>
      <div class="modal" id="prompt">
        <div class="modal-background"></div>
        <div class="modal-content">
          <input class="input" type="text" placeholder="Enter Password">
          <!-- Any other Bulma elements you want -->
        </div>
        <button class="modal-close is-large" aria-label="close" @click="isTeacher"></button>
      </div>
    </div>

  </nav>
</template>

<script>

export default {
  name: "NavBar",
  data(){
    return{
    teacher: 0
    }
  },
  methods:{
    isTeacher(){
      document.getElementById("prompt").classList.toggle("is-active");

    }
  }
}
</script>

<style>
nav{
  display: flex;
  align-items: center;
  justify-content: center;
}

nav .menu-item {
  color: yellow;
  padding: 10px 20px;
  position: relative;
  text-align: center;
  border-bottom: 3px solid transparent;
  transition: 0.4s;
}

nav .menu-item.active,
nav .modal.active,
nav .menu-item:hover{
  background-color: darkviolet;
  border-bottom-color: yellow;
}

nav .menu-item a{
  color: inherit;
  text-decoration: none;
}
</style>
