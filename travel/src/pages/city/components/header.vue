<template>
    <div class='header'>
        城市选择
    <router-link to='/'>
        <div class="iconfont header-icon">&#xe624;</div>
    </router-link>
</div>
</template>

<script>
export default {
    name:'CityHeader'
}
</script>

<style lang="stylus" scoped>
    @import '~styles/varibles.styl';
    .header
        height .86rem
        line-height .86rem
        overflow hidden
        text-align center
        font-size .32rem
        color #ffffff
        background $bgColor

        .header-icon
            position absolute
            width .64rem
            text-align center
            font-size .3rem
            top 0
            left 0
            color #ffffff
</style>