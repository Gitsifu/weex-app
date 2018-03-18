<template>
    <wxc-minibar :title="title"
                 background-color="#009ff0"
                 text-color="#FFFFFF"
                 right-text="更多"
                 @wxcMinibarLeftButtonClicked="minibarLeftButtonClick"
                 @wxcMinibarRightButtonClicked="minibarRightButtonClick"></wxc-minibar>
</template>

<script>
    import { WxcMinibar} from 'weex-ui';
    const modal = weex.requireModule('modal');
    export default {

        name: 'header-bar',
        components: {WxcMinibar},
        props: {
            title: String
        },
        data() {
            return {}
        },
        methods: {
            minibarLeftButtonClick () {
            },
            minibarRightButtonClick () {
                modal.toast({ 'message': 'click rightButton!', 'duration': 1 });
            },
        },
        mounted() {

        }
    }
</script>

<style scoped>

</style>
