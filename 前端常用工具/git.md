# git
- 安装
  + 安装Git之后我们把Git命令也集成到了DOS窗口(MAC苹果系统的终端窗口)
  + git bash here(windows系统有，MAC系统没有)
- 启动windows操作指令(DOS命令)
  + 1.在指定目录中，鼠标右键->git bash here 在当前目录下打开Git命令窗口(只有windows系统有)
  + 2.windows + R 打开DOS窗口，输入cmd也可以进行Git操作
    + 进入到指定的文件目录
      + windows：1.进入到指定的磁盘 磁盘符 例如：E:就是进入到E盘。2.cd 文件目录 进入到指定目录中(可以拖动文件夹到窗口中，自动获取到目录地址)
      + MAC：终端中：cd 文件目录(只有一个磁盘)
- 配置电脑的系统环境变量
  + 在某些指令不能使用的情况下，我们基于系统环境变量的配置，可以使用命令。 计算机右键->属性->高级系统设置->环境变量->path修改为对应的地址
# 初次安装使用git，需要在本地配置一下Git的基本信息(操作git的用户信息)
- 查看本地的git全局配置
  + $ git config -l 查看user.name和user.email
  + 如果信息特别多的时候，我们看不全，一路enter，直到END为止，再次输入:wq保存退出即可
- 配置一下用户名和邮箱(建议用户名和邮箱跟Git-HUB中注册的账号保持一致)
  + $ git config --global user.name 'xxx'
  + $ git config --global user.email 'xxx'
- 查看是否配置成功
  + $ git config --global user.name/user.email 只要能有信息，说明配置成功；否则配置失败，重新配置一下(这个步骤很重要，后期提交到历史区的时候，需要知道谁提交的，此处必须注明本地的用户信息)
- 本地仓库提交到历史区
  + 创建本地仓库 $ git init
  + 把指定的文件从工作区提交到暂存区 $ git add 文件名
    + $ git add . /$ git add -A 把所有工作区的最新修改文件，都提交暂存区
  + 把暂存区的信息提交到历史区，生成一个版本信息 $ git commit -m'备注'(-m和备注之间没有空格)
  > + $ git status 查看文件状态，红色代表工作区，绿色代表暂存区
  > + $ git log/$ git reflog(包括历史回滚信息) 查看本地历史版本信息
  > + $ git reset --hard 版本号(选取版本号的前七位即可)：回滚到指定的历史版本(把制定历史版本中的信息，替换工作区的内容)
  > + $ git rm --cached 文件名 删除传递到暂存区的信息(只是从暂存区移除了，工作区还是有的，用的比较少)

