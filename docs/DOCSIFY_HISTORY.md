# 历程

> 2021.01.01 创建本工程，开始记录技术点滴，让成长看的见。

## docsify 搭建过程

参考官网搭建过程：[quickstart](https://docsify.js.org/#/quickstart)

说明：搭建前需要在自己电脑上安装 npm ，通过 npm 安装 docsify。

> 大神的总结:
>
> 其实npm是nodejs的包管理器（package manager）。我们在Node.js上开发时，会用到很多别人已经写好的javascript代码，如果每当我们需要别人的代码时，都根据名字搜索一下，下载源码，解压，再使用，会非常麻烦。于是就出现了包管理器npm。大家把自己写好的源码上传到npm官网上，如果要用某个或某些个，直接通过npm安装就可以了，不用管那个源码在哪里。并且如果我们要使用模块A，而模块A又依赖模块B，模块B又依赖模块C和D，此时npm会根据依赖关系，把所有依赖的包都下载下来并且管理起来。
> 

也可以不安装npm，官网也提供的手动初始化的操作步骤。具体看：[manual-initialization](https://docsify.js.org/#/quickstart?id=manual-initialization)



### 快速开始

安装 `docsify-cli` ，可以帮助我们初始化和预览本地内容。

```shell
# 安装 docsify-cli 
npm i docsify-cli -g
```

### 初始化

在指定的目录执行初始化命令，帮助我们创建`./docs`子目录，实现文档编写，初始化t命令如下：

```shell
# 初始化命令
docsify init ./docs
```

### 写内容

执行完初始化后，会生成 `./docs`子目录中看到如下文件列表：

- `index.html` ： 入口文件

- `README.md`  ： 作为主页

- `.nojekyll` ：防止GitHub页面忽略以下划线开头的文件

**注**：`README.md`  ： 作为主页，后续我们的内容更新会频繁改动此文件。

除了默认生成的这些文件外，我们还可以创建更多的文件。具体创建可参考官方文档：[more-pages](https://docsify.js.org/#/more-pages)



### 预览站点

当我们修改了本地的文件后，可以使用运行 `docsify serve` 启动服务，预览自己的站点。启动后默认的访问地址为：`http://localhost:3000`.

```shell
# 启动命令
docsify serve docs
```

更多使用 `docsify-cli` 示例，参考[docsify-cli](https://github.com/docsifyjs/docsify-cli).



## docsify 修改记录

> 以下内容记录这个站点的一些修改操作，它是如何一步步变得丰富和有趣的。



### 20210101 开始喽

#### 原始内容

`index.html` 操刀开搞，默认如下：

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Document</title>
  <meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1" />
  <meta name="description" content="Description">
  <meta name="viewport" content="width=device-width, user-scalable=no, initial-scale=1.0, maximum-scale=1.0, minimum-scale=1.0">
  <link rel="stylesheet" href="//unpkg.com/docsify/lib/themes/vue.css">
</head>
<body>
  <div id="app"></div>
  <script>
    window.$docsify = {
      name: '',
      repo: ''  
    }
  </script>
  <script src="//unpkg.com/docsify/lib/docsify.min.js"></script>
</body>
</html>

```

`README.md` 默认内容：

> 进一寸有一寸的欢喜：点亮知识心灯，前方何不柳暗花明——胡适

`.nojekyll` 中默认没有内容

####  修改内容

使用了jquery ,自定义了 java_world_custom css 和 js。

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>JavaWorld</title>
  <meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1" />
  <meta name="viewport" content="width=device-width, user-scalable=no, initial-scale=1.0, maximum-scale=1.0, minimum-scale=1.0">
  <link rel="stylesheet" href="//unpkg.com/docsify/lib/themes/vue.css">
   <!-- web site favicon --->  
  <link rel="icon" href="https://gitee.com/dufyun/java_world_img/raw/master/img/java_world-ico.png" type="image/x-icon">
  <!-- ali iconfont css --->
  <link rel="stylesheet" href="//at.alicdn.com/t/font_1858225_blpnsyrd3lc.css">
  <!-- customer css and js-->
  <link rel="stylesheet" href="css/java_world_custom.css" type="text/css">
  <script src="js/plugin/jquery-1.7.2.min.js"></script>
  <script src="js/java_world_custom.js"></script>
 

  <style type="text/css">
  
  </style>

</head>
<body>
  <!-- 自定义导航  start--->
  <nav>
	<ul>
		<li>
			<a href="#/"><span class="iconfont iconshouye"></span> 首页</a>
		</li>
		<li>
		<a href="#/README?id=基础"><span class="iconfont iconjichu"></span> 基础</a>
			<ul>
				<li>
				<!-- 使用UrlEncode 编码，防止因为emoji表情而不能访问 -->
					<a href="#/README?id=%F0%9F%92%BB%E8%AE%A1%E7%AE%97%E6%9C%BA%E7%BB%84%E6%88%90%E5%8E%9F%E7%90%86">💻计算机组成原理</a>
				</li>
				
				<li>
					<a href="#/README?id=%E2%8C%A8%E8%AE%A1%E7%AE%97%E6%9C%BA%E6%93%8D%E4%BD%9C%E7%B3%BB%E7%BB%9F">⌨计算机操作系统</a>
				</li>
				<li>
					<a href="#/README?id=%F0%9F%8C%90%E8%AE%A1%E7%AE%97%E6%9C%BA%E7%BD%91%E7%BB%9C">🌐计算机网络</a>
				</li>
				
				<li>
					<a href="#/README?id=%F0%9F%92%A0%E8%AE%A1%E7%AE%97%E6%9C%BA%E6%95%B0%E6%8D%AE%E7%BB%93%E6%9E%84">💠计算机数据结构</a>
				</li>
			</ul>
		</li>
		<li>
		 <a href="#/README?id=TODO"><span class="iconfont icontodo-list"></span> TODO...</a>
		</li>
		<!-- 站点历程对应./doc/DOCSIFY_HISTORY.md --->
		<li>
		 <a href="#/DOCSIFY_HISTORY"><span class="iconfont iconjiaqitebieriqi"></span> 站点历程</a>
		</li>
	</ul>
  </nav>
  <!-- 自定义导航  end--->
  
   <div id="app" >加载中🚀🚀🚀</div>
  <script>
    window.$docsify = {
	  nameLink: '/',
      logo: '',// 左侧 logo 图片
      name: '<b>Java🌍World</b>', // 左侧标题名称
      repo: 'https://github.com/dufyun/JavaWorld', // github 仓库地址
	  coverpage: true, // 将coverpage设置为true，创建一个_coverpage.md
	  onlyCover: true, // 只有在访问主页时才加载coverpage
	  auto2top: true, 
	  executeScript: true,
	  topMargin: 90,
	  maxLevel: 4, // 左侧列表展示的层级。默认是6
	  subMaxLevel: 2,
	  search: { //增加搜索框:https://docsify.js.org/#/plugins?id=full-text-search
		paths: 'auto',
        placeholder: '🔎 搜索, 如：Java',
        noData: '🈳 换个关键词试试',
        // Headline depth, 1 - 6
        depth: 6,
		maxAge: 86400000, // Expiration time, the default one day
		hideOtherSidebarContent: true, // whether or not to hide other sidebar content
      },
	  formatUpdated: '{YYYY}/{MM}/{DD} {HH}:{mm}',
	  notFoundPage: '404.md',
	  // 编辑文档
	  /*
      plugins: [
        function(hook, vm) {
          hook.beforeEach(function (html) {
            var url = 'https://github.com/dufyun/JavaWorld/tree/master/' + vm.route.file
              var editHtml = '[📝 EDIT DOCUMENT](' + url + ')\n'
              var editHtml_end = '[🖊 Edit Document](' + url + ')\n'
              return editHtml
                   + html
                   + '\n----\n'
                   + '> Last Modified  '
                   + editHtml_end
          })
        }
      ],
	  */
	  markdown: {
        renderer: {
          code: function(code, lang) {
            if (lang === "dot") {
              return (
                      '<div class="viz">'+ Viz(code, "SVG")+'</div>'
              );
            }
            return this.origin.code.apply(this, arguments);
          }
        }
      },
	  copyCode: { // 拷贝代码提示
          buttonText: '复制请点击',
          errorText: '复制失败',
          successText: '复制成功!'
      },  
	  footer: { // 页脚内容
        copy: ' <span id="siteRunTime"></span> <p/></span> ',
        auth: ' 👨‍⚕️ <strong>© Copyright &copy; 2020.&ensp; <a href="http://www.aflyun.work/" target="_blank">dufyun</a></strong><p/><span>Proudly published with &ensp;  <a href="https://github.com/docsifyjs/docsify" target="_blank">docsify</a>.</span>',
        pre: '<hr/>',
        style: 'text-align: left;',
      },

    }
	
	
  </script>

  </script>
  <!--  <script src="//unpkg.com/docsify/lib/docsify.min.js"></script> -->
  <script src="//cdn.jsdelivr.net/npm/docsify/lib/docsify.min.js"></script>
  <!-- 支持搜索： search -->
  <script src="https://cdn.bootcss.com/docsify/4.5.9/plugins/search.min.js"></script>

 
  <!-- 添加页脚 -->
  <script src="//unpkg.com/docsify-footer-enh/dist/docsify-footer-enh.min.js"></script>
  
 <!-- 复制代码到剪贴板：copyCode ，并搭配复制提醒 -->
  <script src="//cdn.jsdelivr.net/npm/docsify-copy-code"></script>
  
 <!-- 复制提醒：https://sweetalert.bootcss.com/guides/ -->
 <link rel="stylesheet" href="https://cdn.bootcss.com/sweetalert/1.1.3/sweetalert.min.css" type='text/css' media='all' />
  <script src="https://cdn.bootcss.com/sweetalert/1.1.3/sweetalert.min.js"></script>
  <script>
    document.body.oncopy = function () { 
      swal("复制成功 🆒", 
        "若要转载或引用请务必保留原文链接，并申明来源。如果你觉得本仓库不错，那就来 Github 给个 star 吧 😊", 
        "success"); };
  </script>
  <!--代码高亮-->
  <script src="//unpkg.com/prismjs/components/prism-java.js"></script>
  <script src="//cdn.jsdelivr.net/npm/prismjs/components/prism-bash.min.js"></script>


  <script src="js/plugin/jquery.goup.js"></script>
  <script type="text/javascript">
    $(document).ready(function () {
      $.goup({
        trigger: 100,
        bottomOffset: 52,
        locationOffset: 25,
        //title: 'TOP',
        titleAsText: true
      });
    });
  </script>
  <!-- DOT  -->
  <script src="//cdn.jsdelivr.net/npm/viz.js@1.8.0/viz.js"></script>

	
<!-- 缩放图片 -->
<script src="//cdn.jsdelivr.net/npm/docsify/lib/plugins/zoom-image.min.js"></script>

  <!-- 实现离线化，注册 pwa.js -->
  <script>
    if (typeof navigator.serviceWorker !== 'undefined') {
      navigator.serviceWorker.register('pwa.js')
    }
  </script>

</body>
</html>
```



#### 修改总结

- 添加 导航栏 
- 添加 iconfont （操作可参看：[使用阿里矢量图标库操作流程](https://blog.csdn.net/xingfaup/article/details/80333491)）
- 添加 标题样式 
- 添加 favicon.ico
- 添加 covers(封面)，支持多封面，目前只添加一个就行
- 添加搜索功能（搜索还是有点问题）
- 添加页脚
- 添加复制提醒
- 添加回到顶部
- 图片缩放

...


### 20210131 加油喽
#### 修改和添加内容
- 更新首页显示内容和标签
- README 添加了一些分类并添加emoji表情
- 添加如下内容

> [学习方法](StudySkills/StudySkillsCollect.md)

> [思维方式](StudySkills/ThinkIdeaCollect.md)

> [提问技巧](StudySkills/AskQuestionsCollect.md)

上述内容，很多是收集网络好的资源。希望在学习之前，先掌握一些高效的方法和技巧，事半功倍。


### todo...

- [ ]技术体系的大框架完善



#### 备忘

- 在线[urlencode](http://www.jsons.cn/urlencode/)编解码 

  > 用来 编解码 emoji表情

- [使用阿里矢量图标库操作流程](https://blog.csdn.net/xingfaup/article/details/80333491)

  > 使用阿里的矢量图库，如首页上面展示的图标。注意：如何更新了 iconfont 的库，需要重新更新 css 名。
  >
  > <!-- ali iconfont css --->
  >   <link rel="stylesheet" href="//at.alicdn.com/t/font_1858225_z4k22u8cij9.css">

- [docsify plugins](https://docsify.js.org/#/plugins) 插件





## 参考文章

[ocsify 文档构建说明书](https://notebook.js.org/#/docsify/docsifyNotes)

<p/>

---



<b><em><span style="
    font-size: 16px;
    color: #167dba;
">合抱之木，生于毫末；九层之台，起于垒土；千里之行，始于足下。——《老子·道德经》</span></em></b>





