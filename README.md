## spider

版本 v0.0.2

#### 简介
  * 用于抓取微信公众号最新文章生成xml文件

#### 使用
  * git clone https://github.com/buildlove/crawler.git
  * 使用命令行 python weixin_xml.py 或 python weixin_xml.py online
  * 离线使用命令行 python weixin_xml.py offline

>python环境为2.7，依赖插件：BeautifulSoup, json(详见"weixin_xml.py源代码")


#### 注:
  * getHTML函数：请求URL函数成功时打印"加入页面：url"
  * writeFile函数：写入html到指定文件
  * parselink函数：解析节点，寻找微信文章链接
  * wrapPageNode函数：用来获取搜狗搜索的微信号信息列表
  * dict_to_list函数：用来转换dict为list
  * getArticleTitle函数：用来解析搜狗最新文章页面中js片段获取文章的标题和url
  * console函数：以{key:value}的方式打印字典或列表中的字典
  * online函数：控制在线run
  * offline函数：控制离线run
  * main函数：用来控制离线和在线的切换

----------------------------

##版本历史

#### v0.0.2
  * 新增抓取信息生成xml功能
  * 新增计算函数运行时间模块
  * 新增createXML函数创建并解析xml
  * 新增文件xml用来存放抓取的xml

#### v0.0.1
  * 新增离线抓取功能
  * 新增输入微信号，得到微信号列表(dict)和文章列表(list)
  * 新增在线下载，请求url写入请求的html文件为离线下载文件
  * 新增命令行输入python weixin_xml.py offline为离线下载(只有当离线文件存在时才能使用离线请求)
  * 新增命令行输入python weixin_xml.py online为在线下载(默认为在线下载)
  * 新增getHTML函数：请求URL函数成功时打印"加入页面：url"
  * 新增writeFile函数：写入html到指定文件
  * 新增parselink函数：解析节点，寻找微信文章链接
  * 新增wrapPageNode函数：用来获取搜狗搜索的微信号信息列表
  * 新增dict_to_list函数：用来转换dict为list
  * 新增getArticleTitle函数：用来解析搜狗最新文章页面中js片段获取文章的标题和url
  * 新增console函数：以{key:value}的方式打印字典或列表中的字典
  * 新增online函数：控制在线run
  * 新增offline函数：控制离线run
  * 新增main函数：用来控制离线和在线的切换

---------------
## 主要信息
#### 微信号列表(dict)
```
  searchPage  
  name:        #微信名称  
  number:      #微信号  
  artlink:     #微信号文章页面链接  
  funcms:      #微信功能介绍  
  sptit:       #微信认证  
  artSrc:      #微信最新文章链接  
  artTit:      #微信最新文章标题  
```

#### 文章列表(list)
```
  articleList  
  "title":         #文章标题  
  "digest":  
  "content":  
  "fileid":  
  "content_url"    #文章 url  
  "source_url":  
  "cover":  
  "subtype":  
  "is_multi":  
```
