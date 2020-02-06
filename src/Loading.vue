<template>
    <div class="sun-loading" v-show="loading" style="background-color: rgba(0, 0, 0, 0.5);">
        <div class="sun-image"></div>
        <span class="sun-message">{{parentMessage}}</span>
    </div>
</template>

<script>
    export default {
        name: 'loading',
        data() {
            return {
                loading: false,
                parentMessage:'拼命加载中'
            }
        },
        created() {
            let that = this;
            this.bus.$on('loading', function(data,SetMessage) {
                that.parentMessage = SetMessage
                that.loading = !!data;
            })
        }
    }
</script>
