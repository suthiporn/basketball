<template>
  <div class="hello">
    <table border = "0" cellspacing = "0" style="width:400px; height:150px;">
      <tr>
        <td><h1>{{ShowScoreLeft}} &nbsp;&nbsp;
          <img src="http://s3.amazonaws.com/vnn-aws-sites/6261/files/2016/04/6549949d221da550-basketball-hoop-swoosh-clipart-BUTTONCLIPART-355x338.png" width="100px;">
          &nbsp;{{ShowScoreRight}}</h1></td>
      </tr>
    </table>
  </div>
</template>

<script>
export default {
  props: ['ShowScoreLeft', 'ShowScoreRight']
}
</script>
<style scoped>
h1 {
  font-size: 55px;
  color: red; text-shadow: black 0.1em 0.1em 0.2em;
}
table{
  border-radius: 60px;
  background-color: #696969;
}
</style>
