# Homebrew

Q1: Cannot install in Homebrew on ARM processor in Intel default prefix (/usr/local)!

当你用homebrew在配置Apple M1芯片的MacOS里安装应用时，可能会遇到以上问题。解决方案如下：

1. 打开Finder应用
1. 在Applications/Utilities文件夹中找到Terminal.app  
1. 右键菜单选择Get Info
1. 在General中勾选Open using Rosetta
1. 重启Terminal.app之后再运行homebrew

