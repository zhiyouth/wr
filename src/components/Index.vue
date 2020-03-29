<template>
    <div class="index">
        <Tab :data="data" :renderContent="renderContent">
            <h1 slot>我是h1</h1>
        </Tab>
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
            data: [{
                text: '登录'
            }, {
                text: '注册'
            }]
        }
    },
    beforeCreate() {
        console.log('beforeCreate')
    },
    methods: {
        renderContent(index) {
            return `<div>${index}</div>`;
        }
    }
}
</script>

<style scoped>

</style>