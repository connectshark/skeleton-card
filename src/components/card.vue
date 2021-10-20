<template>
<div class="card" :class="{ loading: isLoading }">
  <figure v-if="isLoading"></figure>
  <figure v-else>
    <img src="https://source.unsplash.com/random" alt="random">
  </figure>
  <div class="content" v-if="isLoading">
    <h4></h4>
    <p></p>
  </div>
  <div class="content" v-else>
    <h4>卡片主旨</h4>
    <p>卡片的內容是這樣子的就是一段普通到不行的文字然後需要一點長度所以我就在這裡多輸入一些文字,卡片的內容是這樣子的就是一段普通到不行的文字然後需要一點長度所以我就在這裡多輸入一些文字</p>
  </div>
</div>
</template>

<script>
export default {
  props: {
    isLoading: {
      type: Boolean,
      default: false
    }
  },
  setup () {
    return {

    }
  }
}
</script>

<style lang="scss" scoped>
.card{
  width: 300px;
  margin: auto;
  border-radius: 10px;
  overflow: hidden;
  figure{
    height: 200px;
    img{
      object-fit: cover;
      width: 100%;
      height: inherit;
    }
  }
  .content{
    padding: 20px;
    background-color: #fff;
    h4{
      font-size: 1.5rem;
      line-height: 2rem;
      min-height: 2rem;
      margin-bottom: 20px;
    }
    p{
      font-size: 1rem;
      line-height: 1.5rem;
      min-height: 4rem;
    }
  }
}
.loading{
  figure, h4, p{
    background-color: #dedede;
    background-image: linear-gradient(100deg, #ffffff00 40%, #ffffff99 50%, #ffffff00 60%);
    background-size: 200% 100%;
    background-position-x: 100%;
    animation: loading 1s infinite;
  }
}
@keyframes loading {
  to {
    background-position-x: -20%;
  }
}
</style>