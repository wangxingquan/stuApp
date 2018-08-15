<template>
    <div id="logindiv">
        <div class="box box-info">
            <div class="box-header with-border">
                <h1 class="box-title">Bootstrap</h1>
            </div> 
            <div class="form-horizontal">
                <div class="box-body">
                    <div class="form-group">
                        <label class="col-sm-2 control-label">login</label>
                        <div class="col-sm-10">
                            <input type="text" class="form-control" placeholder="请输入账号" v-bind:value="msgInfo">
                        </div>
                    </div>
                    <div class="form-group">
                        <label class="col-sm-2 control-label">password</label>
                        <div class="col-sm-10">
                            <input type="password" class="form-control" placeholder="请输入密码" value="">
                        </div>
                    </div>
                </div>
                <div class="box-footer">
                    <button class="btn btn-info" style="width: 100%;" @click="toLogin">Sign</button>
                </div>
            </div>
        </div>
    </div>
</template>

<style>
    #logindiv {
        width: 500px;
        margin-left: 65%;
        padding-top: 15%;
    }
    
    .box-info {
        box-shadow: 0px 0px 15px;
    }
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
            alert('起飞');
            this.$router.push({path: '/home'});
        }
    } 
}
</script>

