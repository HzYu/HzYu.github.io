---
layout:     post
title:      安裝Jekyll(Mac)
subtitle:   安裝Jekyll(Mac)
date:       2018-09-05 19:20:33
author:     BY
header-img: img/post-bg-ios9-web.jpg
catalog: true
tags:
    - jekyll
    - Mac
---


我建立的 Blog 是用 [GitHub Pages][GitHub_Pages] + [Jekyll][Jekyll]

首先要先安裝 `Jekyll`

打開 `Terminal`（終端機）

~~~
$ gem install jekyll
~~~

---

在安裝過程中，如果沒有出現以下的錯誤，則忽略

Could not find a valid gem 'jekyll' (>= 0), here is
why: Unable to download data from https://rubygems.org/
SSL_connect returned=1 errno=0 state=SSLv2/v3 read 
server hello A: tlsv1 alert protocol version 
(https://- rubygems.org/latest_specs.4.8.gz)

刪除 SSL 並加入 簡單的HTTP，即可解決

~~~
gem source -a http://rubygems.org
gem source --remove https://rubygems.org 
~~~

___

public_suffix requires Ruby version >= 2.1.

錯誤的意思是 Ruby 版本至少要 >= 2.1

查看目前 Ruby 版本

~~~
Ruby -v
~~~

透過安裝 RVM(管理 Ruby 版本套件) 來升級Ruby版本

進入 [RVM][RVM] 官網



[GitHub_Pages]: https://pages.github.com/
[Jekyll]: https://jekyllrb.com/
[RVM]: https://rvm.io/