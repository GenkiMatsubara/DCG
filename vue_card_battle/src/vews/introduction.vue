<template>
  <div>
    <div class="text">
      <p class="titile">カードを選んでカードを出そう</p>
      <p>タップしたカードでじゃんけんするよ！</p>
      <p>じゃんけんに勝てば相手にダメージ</p>
      <p>あいこだとお互いダメージを受けるぞ</p>
      <p class="titile">相手のHPを0にして勝利しよう！</p>
    </div>
    <div class="btn_box">
      <div class="btn" @click="goInGame()">プレイ！</div>
    </div>
  </div>
</template>

<script>
export default {
  components: {},
  methods: {
    goInGame: function() {
      this.$router.push("InGame");
    }
  }
};
</script>

<style scoped>
.text {
  text-align: center;
  width: 90%;
  margin: 20% auto 0;
}
.titile {
  font-weight: bold;
  font-size: 20px;
}
.btn_box {
  position: absolute;
  bottom: 8%;
  left: 0;
  width: 100%;
}
.btn {
  text-align: center;
  display: block;
  padding: 0.5em 1em;
  text-decoration: none;
  background: #668ad8; /*ボタン色*/
  color: #fff;
  border-bottom: solid 4px #627295;
  border-radius: 3px;
  width: 30%;
  margin: 0 auto;
}
.btn:active {
  /*ボタンを押したとき*/
  -webkit-transform: translateY(4px);
  transform: translateY(4px); /*下に動く*/
  border-bottom: none; /*線を消す*/
}
</style>
