<template>
  <heaeder>
    <div class="navbar">
      <div class="container">
        <div class="navbar-logo">
          Cent
        </div>
        <ul class="navbar-item">
          <li><a href="#">кейсы</a></li>
          <li><a href="#">о нас</a></li>
          <li><a href="#">контакты</a></li>
          <li><a href="#">новости</a></li>
          <li><a href="#">клиенты</a></li>
        </ul>
        <div class="navbar-icon">
          <span></span>
        </div>
      </div>
    </div>
  </heaeder>
</template>

<script>
export default {
  name: "Header"
}
</script>

<style scoped>
.navbar {
  background-color: #0E0E0E;
  width: 100vw;
  color: white;
  position: fixed;
  z-index: 20;
}

.container {
  display: flex;
  justify-content: space-between;
  padding: 40px 15px;
}


ul {
  margin: 0;
  list-style: none;
  display: flex;
  overflow: hidden;
  align-items: flex-start;
}

li {
  margin-left: 20px;
  position: relative;
}

li:after {
  display: block;
  height: 2px;
  width: 100%;
  position: absolute;
  content: "";
  background: white;
  left: 0;
  bottom: 0;
  transform: translateX(800px);
  transition: transform .5s ease;
}


li:hover:after {
  transform: translateX(0);
}

a {
  font-size: 16px;
}

.navbar-logo {
  font-size: 40px;
}

.navbar-icon {
  display: none;
}

@media (max-width: 768px) {
  .navbar-item {
    display: none;
  }

  .navbar-logo {
    font-size: 20px;
  }

  .navbar-icon {
    display: block;
    position: relative;
    width: 28px;
    height: 12px;
  }

  .navbar-icon span {
    background-color: #fff;
    position: absolute;
    width: 100%;
    height: 2px;
    top: 5px;
  }

  .navbar-icon:before,
  .navbar-icon::after {
    content: '';
    background-color: #fff;
    position: absolute;
    width: 100%;
    height: 2px;
    left: 0;
  }

  .navbar-icon:before {
    top: 0;
  }

  .navbar-icon::after {
    bottom: 0;
  }
}

</style>