<template>
  <div class="container">
    <div class="header"><h3>{{ msg }}</h3></div>
    <div class="main">
        <FlashCard/>
    </div>
    <div class="sidebar">sidebar</div>
    <div class="footer">&copy;StudyingIsEasy.com</div>
  </div>
</template>

<script>
import FlashCard from './FlashCard.vue'
export default {
  name: 'Contents',
  components: {
      FlashCard
  },
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.header {
  grid-area: header;
  border-bottom: 1px solid #efefef;
}
.main {
  grid-area: main;
}
.sidebar {
  grid-area: sidebar;
  background-color:darkgray
}
.footer {
  grid-area: footer;
  border-top: 1px solid #efefef;
}

.container {
  display: grid;
  grid-template-columns: 150px auto 150px 150px;
  grid-template-rows: auto;
  grid-template-areas: 
    "header header header header"
    "main main . sidebar"
    "footer footer footer footer";
}
a {
  color: #42b983;
}
</style>
