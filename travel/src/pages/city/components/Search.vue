<template>
    <div class='search'>
        <input type="text" placeholder="输入城市名" class='searchinput'>
    </div>
</template>

<script>
export default {
    name:'CitySearch'
}
</script>

<style lang="stylus" scoped>
    @import '~styles/varibles.styl';

    .search
        height .72rem
        background $bgColor
        padding 0 .1rem

        .searchinput
            height .62rem
            line-height .62rem
            width 100%
            text-align center
            border-radius .06rem
            color #666
</style>