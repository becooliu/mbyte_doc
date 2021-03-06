# mbyte_doc

+ `先fork https://github.com/MByteTech/deal.newkidscenter.org ，然后clone下来`
+ `git submodule update --init`
+ `aws_key` 复制到 `couponsiteengine` 目录下
+ `debug_settings.py` 复制到`/newkidscenter` 目录下

+ `cd` 到项目目录
+ `virtualenv env` 进入虚拟环境

>获取`submodule`
+ `git submodule`

>更新`submodule` 需要哪些就更新哪些
+ `git submodule update --init access_protection/ affiliation/ coupon_site_engine/ text_generation/`

>先执行`setuptools` 升级，再执行后面的操作`
+ `pip install --upgrade setuptools`

>安装相关插件，依次执行三个安装
```
pip install -r text_generation/requirements.txt
pip install -r coupon_site_engine/requirements.txt
pip install -r affiliation/requirements.txt
```
>执行`affiliation` 升级
+ `pip install --upgrade affiliation`

+ 项目跑起来后
   + 进入项目根目录下的项目文件夹（如bonsplans）
   + 打开`urls.py` ,找到`urlpatterns url` 的值（如`suivre/`）
   + 打开同目录下`settings.py` , `REDIRECT_NO_CAMPAIGN_URL_PATTERNS` 的值（如`on`）
   + 将上2步组合成 `suivre/on` 替换原来项目的 `ship/to` (例如替换 `coupon_item_row.html` 页面的)
   + `settings.py` 中 `COUPON_ID_NAME` 值  => `coupon.js` 中两处，以及全局查找替换


*法语网站将 /text_generation/generators/tag_rewriter/tag_rewriter.py 中第36至41行的if 语句删除*
*法语网站settings.py 中 SEARCH_SETTINGS 'index_name': 'coupon-index-fr'，index_name的值后面需要要-fr*

### 报错处理

> 启动时报错找不到`module lxml (' no module named lxml ')`
`pip install lxml`

> `错误1054`
+ 获取服务器上最新的文件。分别`cd`到`affiliation`  `text_generation`  `coupon_site_engine` ，执行 `git pull origin master`

> `cannot import django`
+ 先执行`setuptools` 升级，再手动执行上面`coupon_site_engine` 等三个安装

> `DoesNotExist at /search`
+ 将a.patch 文件复制到coupon_site_engine 目录下，然后执行`git apply a.patch`

> 端口占用查询
+ `ps aux | grep -i manag`

> kill被占用的端口
+ `kill -9 xxxxx`


