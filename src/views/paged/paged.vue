
<template>
    <div class="content">
    <div id="my">
        <div class="card_my">
             <div class="card facebook-card">
                <div class="card-header no-border">
                  <div class="facebook-avatar"><img src="{{card_img}}" width="34" height="34"></div>
                  <div class="facebook-name">夜萧</div>
                  <div class="facebook-date">星期一 3:47pm</div>
                </div>
                <div class="card-content"><img src="{{card_img}}" width="100%"></div>
                <div class="card-footer no-border">
                  <a href="javascript:;" v-on:click="likeBtn" class="link">赞</a>
                  <a href="javascript:;" v-on:click="comment" class="link">评论</a>
                  <a href="javascript:;" v-on:click="shareBtn" class="link">分享</a>
                </div>
              </div>
        </div>
        <div class="card_my_2">
            <div class="card list-block">
                <div class="card-content">
                    <div class="card-content-inner">
                        <div class="row">
                            <div class="col-100">
                                <p>文本3</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <div class="list-block my-menu-1">
            <ul>
                <li>
                    <a v-link="{ path: '/D/toonelevel'}" external class="item-link item-content">
                        <div class="item-media"><i class="icon icon-gift"></i></div>
                        <div class="item-inner">
                            <div class="item-title">演示路由跳转</div>
                        </div>
                    </a>
                </li>
                <li>
                    <a v-link="{ path: '/D/vfor'}" external class="item-link item-content">
                        <div class="item-media"><i class="icon icon-cart"></i></div>
                        <div class="item-inner">
                            <div class="item-title">演示v-for&子路由跳转</div>
                        </div>
                    </a>
                </li>
            </ul>
        </div>

        <div class="list-block" >
            <ul>
                <li>
                    <a v-link="{ path: '/D/vmodel'}" external class="item-link item-content">
                        <div class="item-media"><i class="icon icon-menu"></i></div>
                        <div class="item-inner">
                            <div class="item-title">演示v-model</div>
                        </div>
                    </a>
                </li>
            </ul>
        </div>
        <br />
        <br />
        <br />
    </div>
    </div>
    <router-view>
    </router-view>
</template>
<script>
    module.exports = {
        data: function(){
            return {
                card_img: "http://gqianniu.alicdn.com/bao/uploaded/i4//tfscom/i3/TB10LfcHFXXXXXKXpXXXXXXXXXX_!!0-item_pic.jpg_250x250q60.jpg"
            }
        },
        ready: function () {
            console.log("my-dom准备完毕") // -> 'foo'
        },
        methods:{
            likeBtn:function(){
                alert('调用点赞接口')
            },
            comment:function(){
                alert('调用评论接口')
            },
            shareBtn:function(){
                 alert('调用分享接口')
            }
        }
    }
</script>