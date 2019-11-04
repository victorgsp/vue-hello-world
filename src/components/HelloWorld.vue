<template>
  <div class="hello">
    
    <nav class="navbar navbar-expand-md navbar-dark bg-dark fixed-top"><a href="#" class="navbar-brand"> CESAR</a></nav>
    <main role="main" class="container">
        <div class="starter-template">
            <ul class="list-group">
                <li class="list-group-item active">Horários reservados para sala atual</li>
                <li class="list-group-item" v-for="item in currentRoomReservations" v-bind:key="item">{{ item }}</li>
            </ul>
            <br>
            <ul class="list-group">
                <li class="list-group-item active bold">Salas disponíveis agora</li>
                <li class="list-group-item" v-for="item in anotherFreeRooms" v-bind:key="item">{{ item }}</li>
            </ul>
        </div>
    </main>
  </div>
</template>



<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data(){
    return {
      currentRoomReservations: ["15:30 - 16:30 (01/11/2019)"],
      anotherFreeRooms: [
        "Maria Lencastre - 2°Andar (6 lugares)",
        "Ana Carolina Salgado - 1°Andar (6 lugares)",
        "Auditório - Térreo (80 lugares) ",
        "Casa ",
        "Brum"
      ]};
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
/* h3 {
  margin: 40px 0 0;
}*/
</style>
