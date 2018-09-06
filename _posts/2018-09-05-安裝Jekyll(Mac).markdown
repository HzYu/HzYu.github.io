---
layout:     post
title:      建立Blog - 安裝Jekyll(Mac)
subtitle:   Step1 安裝Jekyll(Mac)
date:       2018-09-05 19:20:33
author:     BY
header-img: img/post-bg-ios9-web.jpg
catalog: true
tags:
    - jekyll
    - Mac
    - Blog
    - GitHub Pages
---


我建立的 Blog 是用 [GitHub Pages][GitHub_Pages] + [Jekyll][Jekyll]

# 安裝Jekyll 

首先要先安裝 `Jekyll`

打開 `Terminal`（終端機）

~~~
$ gem install jekyll
~~~

在安裝過程中，如果沒有出現以下的錯誤，則忽略

---
~~~
Could not find a valid gem 'jekyll' (>= 0), here is
why: Unable to download data from https://rubygems.org/
SSL_connect returned=1 errno=0 state=SSLv2/v3 read 
server hello A: tlsv1 alert protocol version 
(https://- rubygems.org/latest_specs.4.8.gz)
~~~
刪除 `SSL` 並加入簡單的 `HTTP`，即可解決

~~~
gem source -a http://rubygems.org
gem source --remove https://rubygems.org 
~~~

___
~~~
public_suffix requires Ruby version >= 2.1.
~~~
錯誤的意思是 `Ruby` 版本至少要 >= 2.1

查看 `Ruby` 版本是否低於 2.1

~~~
Ruby -v
~~~

## 安裝 RVM

透過安裝 `RVM`(管理 Ruby 版本套件) 來升級 `Ruby` 版本

進入 [RVM][RVM] 官網 按步驟安裝

輸入 `RVM` 官網指定的兩行指令

![](https://ws4.sinaimg.cn/large/0069RVTdgy1fuzxvwixi2j30v00jck1h.jpg)

如果找不到 `gpg`(加密軟體) 指令

在 [gpg][gpg] 官網下載軟體即可

___

`RVM` 安裝完後 就可以使用 `RVM` 升級 `Ruby` 的版本

在終端機下輸入 `rvm list known` 會列出目前有哪些可以安裝的列表

![](https://ws3.sinaimg.cn/large/0069RVTdgy1fuzyrpsp9tj312a11g7bg.jpg)

下載想要 `Ruby` 的版本 

~~~
rvm install ruby-2.3 
~~~

如果安裝過程遇到以下錯誤，可以試試安裝其他 `Ruby` 的版本

~~~
No fallback URL could be found, try increasing 
timeout with:echo "export rvm_max_time_flag=20" >>
~/.rvmrcThere has been an error fetching the ruby 
interpreter. Halting the installation.
~~~

`Ruby` 成功升級完後，輸入指令`Ruby -v`，檢查 `Ruby` 版本是否有成功升級

![](https://ws1.sinaimg.cn/large/0069RVTdgy1fuzyzi3twij312a11g78f.jpg)

確認完 `Ruby` 版本在2.1後，可以開始安裝 `Jekyll`

~~~
gem install Jekyll 
~~~

檢查 `Jekyll` 版本是否有安裝成功

~~~
Jekyll -v
~~~

![](https://ws3.sinaimg.cn/large/0069RVTdgy1fuzzi4lmovj311w0qk41k.jpg)

[GitHub_Pages]: https://pages.github.com/
[Jekyll]: https://jekyllrb.com/
[RVM]: https://rvm.io/
[gpg]: https://gpgtools.org/