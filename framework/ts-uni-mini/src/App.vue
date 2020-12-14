<!--
 * @Author: Li Zhiliang
 * @Date: 2020-12-14 22:36:07
 * @LastEditors: Li Zhiliang
 * @LastEditTime: 2020-12-14 22:53:54
 * @FilePath: /WeChat-Applet/framework/ts-uni-mini/src/App.vue
-->
<script lang="ts">
    // import Vue from 'vue';
    import { Component,Vue ,Watch} from "vue-property-decorator";

    @Component({}) //必须

    // export default Vue.extend({
    //     mpType: 'app',
    //     onLaunch() {
    //         console.log('App Launch')
    //     },
    //     onShow() {
    //         console.log('App Show')
    //     },
    //     onHide() {
    //         console.log('App Hide')
    //     }
    // });
    export default class Index extends Vue {
        
    }
</script>

<style lang="scss">

    @import "uview-ui/index.scss";
    
    /*每个页面公共css */
</style>
