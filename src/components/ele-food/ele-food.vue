<template>
  <div class="food">
    <div class="left">
      <img :src="food.image" alt="" />
    </div>
    <div class="right">
      <span class="name">
        {{ food.name }}
      </span>
      <span class="description">
        {{ food.description }}
      </span>
      <span class="info">
        <span class="sellCount">月售{{ food.sellCount }}份</span>
        <span class="rating">好评率{{ food.rating }}%</span>
      </span>
      <span class="prices">
        <span class="price">{{ food.price }}</span>
        <span class="oldPrice">{{ food.oldPrice }}</span>
      </span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ele-food',
  props: {
    food: Object
  }
};
</script>

<style scoped lang="stylus">
.food
    display flex
    font-size 0
    .left
        flex 0 0 59px
        img
            width 100%
            height 59px
    .right
        margin-left 10px
        flex 1
        display flex
        flex-direction column
        font-size 10px
        color rgba(147,153,159,1)
        .name
            margin-top 2px
            margin-bottom 8px
            font-size 14px
            line-height 14px
            color rgba(7,17,27,1)
        .description
            margin-bottom 8px
        .info
            margin-bottom 8px
            .sellCount
                margin-right 12px
            .rating
                zoom 1


        .prices
            .price
                font-size 14px
                color red
                font-weight 800
                line-height 24px
                margin-right 8px
            .oldPrice
                font-weight 800
                line-height 24px
                text-decoration line-through
</style>
