---
title: Construct blog on github
key: 2018-11-10
tags: study study-github
---


一、 方案选取：
	基于Github Pages, Jekyll

xui.ptlogin2.qq.com

学习使用github
工具：git(msys2), github账号
同步步骤：




学习使用Keepass 管理密码

工具： keepass2软件本身，keepass插件：keepassRPC, chrome插件：kee

学习步骤：
1. 入门keepass2
2. 使用keepass2的触发器，并利用坚果云进行跨平台同步与版本控制（已测试OK）
3. 连接keepass2与Chrome浏览器，学习账号对象的双向存储

学习中出现的问题：
	1. 比预计花费的时间要多的多，还有地址链接拼错导致产生的低级错误
        2. 首选的测试页面错误，首选的插件也过于复杂笨重keepassHTTP+chromeIPass，
           qqmail登录页面情况复杂，应该有拦截、混淆机制在里面，导致始终无法成功

决定使用windows作为开发环境，使用conemu为终端。
使用msys2为命令行平台，fish为工具shell，bash为生产shell。把emacs,git,xxx全都整合进来。
因此，围绕生产的配置和记忆点如下：
1. windows
2. cmder
	1. 修改这几部分（图）
	2. 修改启动shell（图）
3. msys2
	使用前，需配置中科大源。 http://mirrors.ustc.edu.cn/help/msys2.html
4. zsh
	使用git提示，同样的卡顿，不用了
	注意，直接把babun主题粘贴过来，结果错乱。
5. fish（又用回了，不使用主题）(已测试，断了在msys2下使用的念头了，emoji显示错误，卡顿，omf安装后更卡顿)
	插件管理器：oh-my-fish https://github.com/oh-my-fish/oh-my-fish
		主题：dangerous, es
		注意：在msys2下使用出错了
	用户级配置文件的路径：~/.config/fish/config.fish
		注意：config.fish更改后不一定生效，需情况同目录下的缓存文件：fishd.xxx
	fish中兼容地调用bash命令PATTERN：bash -c "arc land --onto `git rev-parse --abbrev-ref HEAD`"
	git的样式theme，需配置一下。https://segmentfault.com/a/1190000015253899
