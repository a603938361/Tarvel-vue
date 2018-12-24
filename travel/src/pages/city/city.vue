<template>
    <div>
        <CityHeader></CityHeader>
        <CitySearch />
    </div>
</template>

<script>
import CityHeader from './components/header'
import CitySearch from './components/Search'


export default {
    name:'City',
    components:{
        CityHeader:CityHeader,
        CitySearch
    }
}
</script>

<style lang="stylus" scoped>
    
</style>