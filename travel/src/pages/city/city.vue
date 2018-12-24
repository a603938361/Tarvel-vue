<template>
    <div>
        <CityHeader></CityHeader>
        <CitySearch />
        <CitySList />
        <CityAlphabet/>
    </div>
</template>

<script>
import CityHeader from './components/header'
import CitySearch from './components/Search'
import CitySList from './components/List'
import CityAlphabet from './components/Alphabet'


export default {
    name:'City',
    components:{
        CityHeader:CityHeader,
        CitySearch,
        CitySList,
        CityAlphabet
    }
}
</script>

<style lang="stylus" scoped>
    
</style>