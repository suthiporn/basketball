<template>
  <div class="hello">
    <table border = "0" cellspacing = "0" style="width:400px; height:150px;">
      <tr>
        <td>
          <button @click="AddButtonLeft1"> +1</button>
          <button @click="AddButtonLeft2"> +2</button>
          <button @click="AddButtonLeft3"> +3</button>
          <button class="deduct"@click="DeductButtonLeft"> -1</button> <br><br>
          <button class="reset" @click="ResetButtonLeft"> Reset</button>
        </td>

        <td>
          <button @click="AddButtonRight1"> +1</button>
          <button @click="AddButtonRight2"> +2</button>
          <button @click="AddButtonRight3"> +3</button>
          <button class="deduct"@click="DeductButtonRight"> -1</button> <br><br>
          <button class="reset" @click="ResetButtonRight"> Reset</button>
        </td>
      </tr>
    </table>


  </div>
</template>

<script>
export default {
  props: ['AddButtonLeft1', 'AddButtonLeft2', 'AddButtonLeft3', 'DeductButtonLeft',
'AddButtonRight1', 'AddButtonRight2', 'AddButtonRight3', 'DeductButtonRight', 'ResetButtonLeft', 'ResetButtonRight']
}
</script>
<style scoped>
h1 {
  color: #42b983;
}
button.reset{
  border-radius: 50%;
  background-color: #00FF00;
  border: 3px solid #696969;
  width: 80px;
  height: 30px;
}
button.reset:hover{
  border: 3px solid #696969;
  background-color: #7CFC00;
  box-shadow: 0 10px 15px 0 rgba(154,205,50,100),0 17px 50px 0 rgba(154,205,50,5);
}
button.deduct{
  border: 2px solid #FF0000;
  background-color: #FF0000;
}
button.deduct:hover{
  border: 2px solid #FF0000;
  background-color: #FF4500;
  box-shadow: 0 10px 15px 0 rgba(255,182,193,1),0 17px 50px 0 rgba(255,182,193,0.1);
}
button{
  width: 40px;
  border: 2px solid #696969;
  background-color: #000080;
  color: #6495ED;
  cursor: pointer;
}
button:hover{
  border: 2px solid #696969;
  background-color: #0000FF;
  box-shadow: 0 10px 15px 0 rgba(0,0,0,0.2),0 17px 50px 0 rgba(0,0,0,0.1);
  color: #000080;
}
</style>
