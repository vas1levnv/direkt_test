<template>
  <div class="ourClients">
    <div class="container">
      <h2>Наши клиенты</h2>
    </div>
    <div class="clients">
      <div class="right">
        <Clients/>
      </div>
      <div class="left">
        <Clients/>
      </div>
      <div class="right">
        <Clients/>
      </div>
      <div class="left">
        <Clients/>
      </div>
    </div>
  </div>

</template>

<script>
import Clients from "@/components/OurClients/Clients";

export default {
  components: {Clients},
  name: "OurClients"
}
</script>

<style scoped>
* {
  background: #0E0E0E;
  color: white;

}

.ourClients {
  padding: 140px 0;
  z-index: 10;
  position: relative;

}

.clients {
  overflow-x: auto;
}

.right {
  padding-left: 300px;
  position: relative;
  top: 0;

}

.left {

  position: relative;
  top: 0;
}

@media (max-width: 768px) {
  .ourClients {
    padding: 40px 0;
  }
}

</style>