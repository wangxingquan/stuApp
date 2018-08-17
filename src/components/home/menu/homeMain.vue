<template>
    <div class="maindiv">
        <div class="headNav">
            <div class="tree well">
                <ul>
                    <li>
                        <span><i class="glyphicon glyphicon-folder-open"></i> 后台管理</span>
                        <ul>
                            <li>
                                <a @click="clickUser"><span><i class="glyphicon glyphicon-leaf"></i> 用户</span></a>
                            </li>
                            <li>
                                <a @click="clickRole"><span><i class="glyphicon glyphicon-leaf"></i> 角色</span></a>
                            </li>
                            <li>
                                <a href=""><span><i class="glyphicon glyphicon-leaf"></i> 日志</span></a>
                            </li>
                        </ul>
                    </li>
                </ul>
            </div>
        </div>
        <div class="content" v-show="isShowWell">
            <div class="center">
                <h2>Wellcome to here,bootstrap family</h2>
            </div>
        </div>
        <div class="content" v-show="isShowUser">
            <div class="row">
                <div class="center">
                    <h2>用户列表</h2>
                </div>
                <div class="col-sm-12">
                    <div class="input-group" style="width: 380px;padding-left:13.5px;">
                        <input type="text" class="form-control pull-right" placeholder="关键字查询">
                        <div class="input-group-btn">
                            <button class="btn btn-default"><i class="glyphicon glyphicon-search"></i></button>
                        </div>
                        <div class="input-group-btn right" style="padding-left:20px;width: 100px;">
                            <button class="btn btn-info">新增</button>
                        </div>
                    </div>
                </div>
            </div>
            <div class="col-sm-12">
                <table class="table table-bordered table-hover dataTable center" role="grid">
                    <colgroup>
                        <col width="10" />
                        <col width="50" />
                        <col width="50" />
                        <col width="50" />
                        <col width="50" />
                    </colgroup>
                    <thead>
                        <tr>
                            <td>#</td>
                            <td>userName</td>
                            <td>telphone</td>
                            <td>createTime</td>
                            <td>button</td>
                        </tr>
                    </thead>
                    <tbody>    
                        <tr>
                            <td>1</td>
                            <td>json</td>
                            <td>11111</td>
                            <td>2018-08-17</td>
                            <td>
                                <a href="#" class="btn btn-xs btn-warning">修改</a>
                                <a href="#" class="btn btn-xs btn-info">删除</a>
                            </td>
                        </tr>
                        <tr>
                            <td>2</td>
                            <td>luxi</td>
                            <td>11111</td>
                            <td>2018-08-17</td>
                            <td>
                                <a href="#" class="btn btn-xs btn-warning">修改</a>
                                <a href="#" class="btn btn-xs btn-info">删除</a>
                            </td>
                        </tr>
                        <tr>
                            <td>3</td>
                            <td>laien</td>
                            <td>11111</td>
                            <td>2018-08-17</td>
                            <td>
                                <a href="#" class="btn btn-xs btn-warning">修改</a>
                                <a href="#" class="btn btn-xs btn-info">删除</a>
                            </td>
                        </tr>
                    </tbody>  
                </table>
            </div>
        </div>

        <div class="content" v-show="isShowRole">
            <div class="row">
                <div class="center">
                    <h2>角色列表</h2>
                </div>
                <div class="col-sm-12">
                    <div class="input-group" style="width: 380px;padding-left:13.5px;">
                        <input type="text" class="form-control pull-right" placeholder="关键字查询">
                        <div class="input-group-btn">
                            <button class="btn btn-default"><i class="glyphicon glyphicon-search"></i></button>
                        </div>
                        <div class="input-group-btn right" style="padding-left:20px;width: 100px;">
                            <button class="btn btn-info">新增</button>
                        </div>
                    </div>
                </div>
            </div>
            <div class="col-sm-12">
                <table class="table table-bordered table-hover dataTable center" role="grid">
                    <colgroup>
                        <col width="10" />
                        <col width="50" />
                        <col width="50" />
                        <col width="50" />
                        <col width="50" />
                    </colgroup>
                    <thead>
                        <tr>
                            <td>#</td>
                            <td>roleName</td>
                            <td>roleCode</td>
                            <td>createTime</td>
                            <td>button</td>
                        </tr>
                    </thead>
                    <tbody>    
                        <tr>
                            <td>1</td>
                            <td>json</td>
                            <td>code1</td>
                            <td>2018-08-17</td>
                            <td>
                                <a href="#" class="btn btn-xs btn-warning">修改</a>
                                <a href="#" class="btn btn-xs btn-info">删除</a>
                            </td>
                        </tr>
                        <tr>
                            <td>2</td>
                            <td>luxi</td>
                            <td>code2</td>
                            <td>2018-08-17</td>
                            <td>
                                <a href="#" class="btn btn-xs btn-warning">修改</a>
                                <a href="#" class="btn btn-xs btn-info">删除</a>
                            </td>
                        </tr>
                        <tr>
                            <td>3</td>
                            <td>laien</td>
                            <td>code3</td>
                            <td>2018-08-17</td>
                            <td>
                                <a href="#" class="btn btn-xs btn-warning">修改</a>
                                <a href="#" class="btn btn-xs btn-info">删除</a>
                            </td>
                        </tr>
                    </tbody>  
                </table>
            </div>
        </div>

    </div>
</template>

<script>
export default {
    data(){
        return {
            isShowWell: true,
            isShowUser: false,
            isShowRole: false,
            isShowLog: false,
        }
    },
    methods: {
        clickUser: function() {
            this.isShowWell = false;
            this.isShowUser = true;
            this.isShowRole = false;
        },
        clickRole: function() {
            this.isShowWell = false;
            this.isShowUser = false;
            this.isShowRole = true;
        }
    },
};

$(function() {
  $(".tree li:has(ul)")
    .addClass("parent_li")
    .find(" > span")
    .attr("title", "Collapse this branch");
  $(".tree li.parent_li > span").on("click", function(e) {
    var children = $(this)
      .parent("li.parent_li")
      .find(" > ul > li");
    if (children.is(":visible")) {
      children.hide("fast");
      $(this)
        .attr("title", "Expand this branch")
        .find(" > i")
        .addClass("icon-plus-sign")
        .removeClass("icon-minus-sign");
    } else {
      children.show("fast");
      $(this)
        .attr("title", "Collapse this branch")
        .find(" > i")
        .addClass("icon-minus-sign")
        .removeClass("icon-plus-sign");
    }
    e.stopPropagation();
  });
});
</script>


