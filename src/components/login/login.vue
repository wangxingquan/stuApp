<template>
    <div class="loginStyle">
        <div class="box box-info">
            <div class="with-border">
                <h1 class="box-title">Bootstrap</h1>
            </div> 
            <div class="form-horizontal">
                <div class="box-body">
                    <div class="form-group">
                        <div class="col-sm-10">
                            <input type="text" class="form-control" placeholder="login" >
                        </div>
                    </div>
                    <div class="form-group">
                        <div class="col-sm-10">
                            <input type="password" class="form-control" placeholder="password" value="">
                        </div>
                    </div>
                </div>
                <div class="box-footer">
                    <button class="btn btn-info" style="width: 50%;" @click="toLogin">Sign me in</button>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
    @import '../../assets/css/common/login.css'; 
</style>

<script>
export default {
    data: function () {
        return {
            msgInfo: 'wellcome',
        }
    },
    methods: {
        toLogin: function() {
            console.log("点击了登录按钮，path:/home");
            this.$router.push({path: '/home'});
        }
    } 
}
</script>

