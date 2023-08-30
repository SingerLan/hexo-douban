# hexo-douban
hexo豆瓣我看过的电影

#效果图
  ![image](https://github.com/SingerLan/hexo-douban/assets/44799711/3e96a3c9-47fa-434f-aa36-1d2a56b06157)
#代码截图
  ![image](https://github.com/SingerLan/hexo-douban/assets/44799711/938e6b26-51c6-4bc2-8414-b568d3b9c755)
#效果网址
  https://singerlan.gitee.io/more/
#步骤

  ## 新建movie.js文件 

    ```
    /**
     * movie.js v1 | https://github.com/SingerLan/hexo-douban/
     * 格式与官方标签插件一致使用空格分隔，中括号内的是可选参数（中括号不需要写出来）
     *
     * {% movie %}
     * {% movie %}
     */
    'use strict';
    
    module.exports = ctx => function(args, content) {
      var el = '<h1 style="text-align: center;">豆瓣我看过的电影</h1>'
      el += '<script type="text/javascript">'
      el += "var head = document.getElementsByTagName('head')[0];"
      el += "var link = document.createElement('link');"
      el += "link.type='text/css';"
      el += "link.rel = 'stylesheet';"
      el += "link.href = '/libs/DoubanBoard/DoubanBoard.04.css';"
      el += "head.appendChild(link);"
      el += "</script>"
      el += "<script>var DoubanPageSize=20;</script>"
      el += '<script type="text/javascript" src="https://gcore.jsdelivr.net/npm/jquery@3.6.2/dist/jquery.min.js"></script>'
      el += '<script type="text/javascript" src="/libs/DoubanBoard/DoubanBoard.04.js"></script>'
      el += '<div id="douban-movie-list" class="doubanboard-list"></div>'
      return el
    }
    ```

 ## DoubanBoard.04.js
      https://gitee.com/SingerLan/douban/blob/master/assets/DoubanBoard.04.js
 ## DoubanBoard.04.css
      https://gitee.com/SingerLan/douban/blob/master/assets/DoubanBoard.04.css

 ## 采集文件
     https://github.com/SingerLan/douban-wordpress
     将所有文件上传到 replit
 ## 调用
     修改 https://gitee.com/SingerLan/douban/blob/master/assets/DoubanBoard.04.js
     97行地址为replit 地址。
 ## 发布

 ## replit介绍
      Replit是一家公司，提供在线运行和分享多种编程语言代码的工具，包括Python、Ruby、JavaScript、Java等等。该公司为教育工作者、学习者和开发人员构建简单的工具和平台。Replit于2016年由程序员Amjad Masad、Faris Masad和设计师Haya Odeh在旧金山成立。Replit宣称自己是“第一个完全在线的多人计算环境”，可以让任何人在最小的准备和无需下载的情况下开始编码
      地址 https://replit.com/

      
