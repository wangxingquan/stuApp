<template>
    <div class="maindiv">
        <div class="headNav">
            <div class="tree well">
                <ul>
                    <li>
                        <span><i class="glyphicon glyphicon-folder-open"></i> 娱乐列表</span>
                        <ul>
                            <li>
                                <a @click="toMovie"><span><i class="glyphicon glyphicon-leaf"></i> 电影</span></a>
                            </li>
                            <li>
                                <a @click="toAline"><span><i class="glyphicon glyphicon-leaf"></i> 直播</span></a>
                            </li>
                            <li>
                                <a @click="toNBA"><span><i class="glyphicon glyphicon-leaf"></i> NBA</span></a>
                            </li>
                        </ul>
                    </li>
                </ul>
            </div>
        </div>

        <div class="content" v-show="isShowWell">
            <div class="center">
                <h2>Wellcome to Yule,bootstrap family</h2>
            </div>
        </div>

        <div class="content" v-show="isMovie">
            <div class="center">
                <h2>Movie List</h2>
            </div>

            <div class="row">
                <div class="col-sm-10">
                    <div class="input-group" style="width: 480px;padding-left:13.5px;">
                        <dl>
                            <dt>下载地址</dt>
                            <dd><a href="#">电影巴士</a></dd>
                            <dt>在线地址</dt>
                            <dd><a href="#">银月游戏</a></dd>
                        </dl>
                    </div>    
                </div>
            </div>
        </div>

        <div class="content" v-show="isAline">
            <div class="center">
                <h2>Aline List</h2>
            </div>

            <div class="row">
                <div class="col-sm-10">
                    <div class="input-group" style="width: 480px;padding-left:13.5px;">
                        <dl>
                            <dt>直播地址</dt>
                            <dd><a href="#">斗鱼</a></dd>
                            <dd><a href="#">虎牙</a></dd>
                            <dt>主播</dt>
                            <dd><a href="#">狂老弟</a></dd>
                        </dl>
                    </div>    
                </div>
            </div>
        </div>

    </div> 
</template>

<style scoped>
    dd {
        margin-left: 44px;
        padding: 20px 20px;
    }
</style>


<script>
export default {
    data() {
        return {
            isShowWell: false,
            isMovie: true,
            isAline: false,
            isNBA: false,
        }
    },
    methods: {
        toMovie: function() {
            this.isShowWell = false;
            this.isAline = false;
            this.isNBA = false;
            this.isMovie = true;
        },
        toAline: function() {
            this.isShowWell = false;
            this.isMovie = false;
            this.isNBA = false;
            this.isAline = true;
        },
        toNBA: function() {
            alert("开发中....");
        }
    }
}
</script>

