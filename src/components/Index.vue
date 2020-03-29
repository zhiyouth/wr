<template>
    <div class="index">
        <Tab :data="data"/>
        Index
    </div>
</template>

<script>
import Tab from '../common-components/Tab';
export default {
    name: 'Index',
    components: {
        Tab
    },  
    data () {
        return {
            data: [{}, {}, {}]
        }
    },
    beforeCreate () {
        console.log('beforeCreate')
    }
}
</script>

<style scoped>

</style>