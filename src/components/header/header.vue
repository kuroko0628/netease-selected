<template>
  <div id="header">
    <div class="left">
      <router-link to="/firstView/recommended">
        <van-icon name="wap-home-o" size="26" color="#666"/>
      </router-link>
    </div>
    <div class="mid">
			<span v-if="title">{{title}}</span>
			<slot name="mid"></slot>
		</div>
    <div class="right">
		<router-link to="/wysearch">
			<van-icon class="search" name="search" size="26" color="#666"/>
		</router-link>
		<router-link to="/shopCart">
			<van-icon name="shopping-cart-o" size="26" color="#666"/>
		</router-link>
		</div>
  </div>
</template>

<script>
export default {
	name:'Header',
  props: ["title"],
  data() {
    return {};
  }
};
</script>

<style lang="stylus">
	#header
		background-color #fafafa
		padding 0 20px
		line-height 90px
		height 90px
		border-bottom 1px solid #ddd
		display flex
		justify-content space-between
		.left
			width 126px
			padding-top 18px
		.mid
			font-size 38px
		.right
			width 126px
			padding-top 18px
			.search
				margin-right 20px
</style>
