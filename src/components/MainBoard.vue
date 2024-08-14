<template>
  <div class="MainBoard">
    <div class="MainOne">
      <h4>Wallet Recharged</h4>
      <input
        v-model.number="walletRecharged"
        @input="UpdateValue"
        type="text"
        id="inputWidgetOne"
        placeholder="₹ 0.00"
      />
    </div>
    <div class="MainTwo">
      <h4>Amount Spent</h4>
      <input type="text" id="inputWidgetTwo" placeholder="₹ 0.00" />
    </div>
    <div class="MainThree">
      <h4>Balance</h4>
      <input type="text" id="inputWidgetThree" placeholder="₹ 0.00" />
    </div>
    <div class="MainFour">
      <h4>Expenses</h4>
      <input type="text" id="inputWidgetFour" placeholder="₹ 0.00" />
    </div>
  </div>
</template>
<script>
export default {
  data(){
    return{
      walletRecharged: 0
    }

  },
  // method: {
  //   UpdateValue{
  //     this.chartData.dataset[3].data.push(this.newValue)
  //     console.log(this.walletRecharged)
  //   }
  // }
}
</script>

<style>
#value {
  display: flex;
  justify-content: center;
  align-items: center;
}

body {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  position: relative;
  padding: 10px;
}

.MainBoard {
  position: absolute;
  /* left: 220px; */
  top: 85px;
  left: 260px;
  right: -290px;
  height: 11rem;
  width: 78rem;
  background: #f1f2f6;
  display: flex;
  justify-content: space-around;
  border-radius: 20px; /* Rounded corners */
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1); /* Soft shadow */
}

.MainOne {
  position: relative;
  top: 15px;
  padding: 10px;
  left: 20px;
  height: 130px;
  width: 200px;
  background: #b8e994;
  border-radius: 25px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1); /* Soft shadow */
  transition: all 0.3s ease; /* Smooth transition */
}

.MainTwo {
  position: relative;
  top: 15px;
  padding: 10px;
  left: 20px;
  height: 130px;
  width: 200px;
  background: #f6e58d;
  border-radius: 25px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1); /* Soft shadow */
  transition: all 0.3s ease; /* Smooth transition */
}

.MainThree {
  position: relative;
  top: 15px;
  padding: 10px;
  left: 20px;
  height: 130px;
  width: 200px;
  background: #f3a683;
  border-radius: 25px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1); /* Soft shadow */
  transition: all 0.3s ease; /* Smooth transition */
}

.MainFour {
  position: relative;
  top: 15px;
  padding: 10px;
  left: 20px;
  height: 130px;
  width: 200px;
  background: rgba(255, 159, 243);
  border-radius: 25px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1); /* Soft shadow */
  transition: all 0.3s ease; /* Smooth transition */
}

#inputWidgetOne {
  height: 45px;
  width: 180px;
  background: #b8e994;
  border: 1px solid rgba(184, 233, 148, 0.5);
  color: black;
  position: relative;
  left: 10px;
  font-size: larger;
  font-size: 35px;
  font-weight: 800;
}

#inputWidgetTwo {
  height: 45px;
  width: 180px;
  background: #f6e58d;
  border: 1px solid rgba(246, 229, 141, 0.5);
  color: black;
  position: relative;
  left: 10px;
  font-size: larger;
  font-size: 35px;
  font-weight: 800;
}
#inputWidgetThree {
  height: 35px;
  width: 180px;
  background: #f3a683;
  border: 1px solid rgba(243, 166, 131, 0.5);
  color: black;
  position: relative;
  left: 10px;
  font-size: 35px;
  font-weight: 800;
}
#inputWidgetFour {
  height: 35px;
  width: 180px;
  background: rgba(255, 159, 243);
  border: 1px solid rgba(255, 159, 243, 0.1);
  color: black;
  position: relative;
  left: 10px;
  font-size: larger;
  font-size: 35px;
  font-weight: 800;
}
</style>
