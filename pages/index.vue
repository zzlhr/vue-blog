<template>
  <b-container>
    <div class="row">
      <div class="col-lg-8 blog-content">
        <div class="blog-list">
          <div class="blog-item" v-for="article in articles" :key="article.articleId">
            <div class="blog-content">
              <h5 class="blog-content-title"><a href="article/123/">{{article.articleTitle}}</a></h5>
              <!--<small>由 lhr 发表于 2018-7-7 13:20:03 更新与 2018-7-7 13:20:03    点击数: 20    评论数: 0    点赞数: 0</small>-->
              <p class="blog-content-describe">{{article.articleDescribe}}</p>
              <div class="blog-content-footer">
                <span href="about"><i class="iconfont icon-tagfill"></i>&nbsp;<a href="Mac">Mac</a></span>
                <span><i class="iconfont icon-myfill"></i>&nbsp;<a href="about/lhr/">{{article.articleAuthor.name}}</a></span>
                <span href="about"><i class="iconfont icon-msnui-time-bold"></i>&nbsp;{{article.createTime}}</span>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="col-lg-3 blog-right">
        <div class="blog-list blog-right-list">
          <div class="blog-item">
            <label class="blog-item-title">站长信息</label>
            <div class="blog-item-body">
              <p class="h6">刘浩然</p>
              <p>
                一个资深技术宅的站点
              </p>
              <div class="blog-link">
                <a href="mailto:lhr@lhrsite.com"><i class="iconfont icon-mail"></i></a>
                <a href="https://github.com/zzlhr/"><i class="iconfont icon-github"></i></a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </b-container>
</template>

<script>
import AppLogo from '~/components/AppLogo.vue'

export default {
  components: {
    AppLogo
  },
  data(){
    return {
      articles:[
        {
          articleId:1,
          articleTitle: 'IDEA 正则批量替换',
          articleDescribe:'场景给实体类批量添加默认值，属性多加上类型多手动换起来太麻烦。',
          articleAuthor:{
            id:1,
            name: 'lhr'
          },
          createTime:'2018-06-13 11:43:42'
        },
        {
          articleId:2,
          articleTitle: 'apache ab 压力测试工具-1',
          articleDescribe:'记录apache ab学习使用过程.',
          articleAuthor:{
            id:1,
            name: 'lhr'
          },
          createTime:'2018-05-17 14:51:21'
        },
        {
          articleId:3,
          articleTitle: 'vue-resource出现Cannot read property \'post\' of undefined得解决方案',
          articleDescribe:'使用webpack打包按照官方文档引用出现\'post\' of undefined的解决方案。',
          articleAuthor:{
            id:1,
            name: 'lhr'
          },
          createTime:'2018-05-04 09:06:58'
        }

      ]
    }
  }
}
</script>

<style>
.b-container{
  display: flex;
  flex-wrap: nowrap;
  flex-direction: row;
}
</style>
