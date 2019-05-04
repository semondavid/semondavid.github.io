---
layout: post
title: MARKDOWN文件实时编辑预览
---

#MARKDOWN文件实时编辑预览
##0.packagecontrol
进入包安装官网：[https://packagecontrol.io/installation]，提示最简单的方式是用Ctrl+`的快捷方式打开控制台，并且复制粘贴下面一段代码

`import urllib.request,os,hashlib; h = '6f4c264a24d933ce70df5dedcf1dcaee' + 'ebe013ee18cced0ef93d5f746d80ef60'; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); by = urllib.request.urlopen( 'http://packagecontrol.io/' + pf.replace(' ', '%20')).read(); dh = hashlib.sha256(by).hexdigest(); print('Error validating download (got %s instead of %s), please try manual install' % (dh, h)) if dh != h else open(os.path.join( ipp, pf), 'wb' ).write(by)`

如果因为网络限制等原因不可用，可以尝试手动安装包管理工具

* `Preferences > Browse Packages…`进入包目录
* 进入上一级`Installed Packages`目录
    - 下载[Package Control.sublime-package](https://packagecontrol.io/Package%20Control.sublime-package)
    - 然后将其粘贴到`Installed Packages`目录
* 最后重启SubimeText3.

##1.安装三个包
`Ctrl+Shift+P`然后输入`pcip`进入包管理，输入下方三个包名称进行安装

- Markdown Editing 
- Markdown Preview
- auto-save


##2.配置md文件预览刷新
在md文件尾部添加刷新语句
`<meta http-equiv="refresh" content="1">`
##3.打开自动保存
`Ctrl+Shift+P`打开包管理工具，输入auto，找到`Toggle AutoSave:Current File Only`并回车选中

可以在Package Setting中配置Auto-Save的Settings-users参数：
`"auto_save_delay_in_seconds": 0.15`





参考文档：[使用Sublime Text 3进行Markdown 编辑+实时预览](https://blog.csdn.net/github_32886825/article/details/52930195)
