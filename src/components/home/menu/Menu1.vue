<template>
    <div class="leftdiv">
        <nav class="navbar-inverse visible-lg visible-md" role="navigation">
        <div class="container">
            <div class="navbar-header">
                <a class="navbar-brand" href="#">Not</a>
            </div>
            <div>
                <ul class="nav navbar-nav">
                    <li class="active"><a @click="toHomeMain">后台管理</a></li>
                    <li><a href="#">学习空间</a></li>
                    <li><a @click="toYule">娱乐天地</a></li>
                </ul>
            </div>
        </div>
    </nav>

    <div v-show="statusJson.isHome">
        <main1></main1>
    </div> 

    <div v-show="statusJson.isYule">
        <yule></yule>
    </div>

    </div>
</template>

<style scoped>
    @import url("menu.css");
</style>

<script>
import homeMain from "./homeMain";
import Yule from "./Yule";
export default {
    data() {
        return {
            statusJson: {
                isHome: true,
                isYule: false,
            },
        }
    },
    components: {
        main1: homeMain,
        yule: Yule,
    },
    methods: {
        toYule: function(){
            this.statusJson.isHome = false;
            this.statusJson.isYule = true;
        },
        toHomeMain: function(){
            this.statusJson.isHome = true;
            this.statusJson.isYule = false;
        }
    }
}
</script>


