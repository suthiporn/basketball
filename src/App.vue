<template>
  <div id="app">
    <bas-header></bas-header>
    <bas-score :show-score-left="ShowScoreLeft" :show-score-right="ShowScoreRight"></bas-score>
    <bas-button :add-button-left1="AddButtonLeft1" :add-button-left2="AddButtonLeft2"
    :add-button-left3="AddButtonLeft3" :deduct-button-left="DeductButtonLeft"
    :add-button-right1="AddButtonRight1" :add-button-right2="AddButtonRight2"
    :add-button-right3="AddButtonRight3" :deduct-button-right="DeductButtonRight"
    :reset-button-left="ResetButtonLeft" :reset-button-right="ResetButtonRight"></bas-button>
  </div>
</template>

<script>
import BasHeader from './components/BasHeader'
import BasScore from './components/BasScore'
import BasButton from './components/BasButton'
export default {
  components: {
    BasHeader,
    BasScore,
    BasButton
  },
  data () {
    return {
      ShowScoreLeft: 0,
      ShowScoreRight: 0
    }
  },
  methods: {
    AddButtonLeft1 () {
      this.ShowScoreLeft++
    },
    AddButtonLeft2 () {
      this.ShowScoreLeft = this.ShowScoreLeft + 2
    },
    AddButtonLeft3 () {
      this.ShowScoreLeft = this.ShowScoreLeft + 3
    },
    DeductButtonLeft () {
      this.ShowScoreLeft--
      if (this.ShowScoreLeft < 0) {
        this.ShowScoreLeft = 0
      }
    },
    AddButtonRight1 () {
      this.ShowScoreRight++
    },
    AddButtonRight2 () {
      this.ShowScoreRight = this.ShowScoreRight + 2
    },
    AddButtonRight3 () {
      this.ShowScoreRight = this.ShowScoreRight + 3
    },
    DeductButtonRight () {
      this.ShowScoreRight--
      if (this.ShowScoreRight < 0) {
        this.ShowScoreRight = 0
      }
    },
    ResetButtonLeft () {
      this.ShowScoreLeft = 0
    },
    ResetButtonRight () {
      this.ShowScoreRight = 0
    }
  }
}
</script>

<style>
html {
  height: 100%;
}

body {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100%;
}

#app {
  color: #2c3e50;
  margin-top: -100px;
  max-width: 600px;
  font-family: Source Sans Pro, Helvetica, sans-serif;
  text-align: center;
}

#app a {
  color: #42b983;
  text-decoration: none;
}

.logo {
  width: 100px;
  height: 100px
}
</style>
