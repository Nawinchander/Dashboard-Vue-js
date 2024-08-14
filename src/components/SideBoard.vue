<template>
    <div class="sideBar">
        <div class="img">
            <img src="./Images/UserImage.png" alt="">
        </div>
        <div class="account">
            <h3>{{ name }}</h3>
            <h5>{{ email }}</h5>
        </div>
        <div class="listValue">
        <ul>
            <ul><a href="#">Home</a></ul>
            <ul><a href="#">Wallet</a></ul>
            <ul><a href="#">Balance</a></ul>
            <ul><a href="#">Expenses</a></ul>
          </ul>
        </div>
    </div>
</template>

<script>
export default {
  data () {
    return {
      name: 'Nawin',
      email: 'nawin@gmail.com'
    }
  }
}
</script>

<style>
body{
    margin: 0;
    padding: 0px;
    position: relative;
}
.sideBar{
    background:#dff9fb;
    height: 66rem;
    width: 195px;
    position: absolute;
    left: 13px;
    top: 82px;
    padding: 20px;
    border-radius: 20px; /* Rounded corners */
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1); /* Soft shadow */
}

img{
    position: relative;
    left: 3px;
    top: 20px;
    border-radius: 600px;

}

.account{
    margin: 0px;
    padding: 10px;
    position: relative;
    left: 25px;
}

h3{
    position: relative;
    font-weight: bolder;
    position: relative;
    left: 27px;
}
h5{
    position: relative;
    right: 5px;
}

a{
    text-decoration: none;
    color: black;
    justify-content: space-between;
    margin: 10px;
    position: relative;
    display: block;
    right: 35px;
    transition: background-color 0.3s, color 0.3s;
    /* border: 2px solid black; */
}

a:hover{
    color: blue;
}

ul{
    margin: 0px;
    text-decoration: none;
    color: black;

}

</style>
