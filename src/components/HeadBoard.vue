<template>
  <div class="heading">
    <div class="title">
      <h1 id="Nboard">N-Board</h1>
    </div>
    <div class="analytics">
      <h3 id="Nboard">Analytics</h3>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap");
body {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
  font-family: "Poppins", sans-serif;
  position: relative;
}

#Nboard:hover {
  color: #d63031;
}

.heading {
  padding: 0;
  margin: 0;
  height: 100px;
  width: 100vw;
  top: -22px;
  background: #81ecec;
  position: relative;
}

.title {
  position: absolute;
  left: 50px;
  top: 15px;
}

.analytics {
  position: absolute;
  display: flex;
  justify-content: end;
  right: 120px;
  top: 25px;
}
</style>
