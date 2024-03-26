# Git

## 一、工作区域与文件状态

### 原理图

![](E:\Typora\git学习\img\Snipaste_2024-03-25_09-19-12.png)

工作区：文件管理器中能看到的区域（用ls指令可查看）
暂存区：由工作区的文件添加 （用git status查看暂存区情况）
本地仓库：由暂存区提交（存储各次提交的版本信息）（用git log可查看各次提交信息，git ls-files查看仓库状态）

![](img/Snipaste_2024-03-25_12-09-39.png)

## 二、git指令

![](img/Snipaste_2024-03-25_11-55-54.png)



git add *.txt：这个指令可以批量添加工作区的TXT文件到暂存区
git add .：添加当前所以工作区文件到暂存区

git commit -m "此处写提交信息的记录"
这个指令只会（提交）存储暂存区的文件，不会提交工作区



![](img/Snipaste_2024-03-25_18-53-04.png)



git reset用于回溯到某一历史记录（根据对应的版本号），git reflog可查看所有历史提交操作及其对应的版本号
![](img/git reset回溯的3种模式.png)



git diff
![](img/git diff版本之间差异比较.png)

git rm(删除后还要git commit提交才能从版本库中也删除)
![](img/git rm删除文件.png)

.gitignore：把不希望提交的文件添加到.gitignore文件中，则可以在提交时被忽略
![](img/文件忽略.png)

![](img/.gitignore匹配规则.png)

git push & git pull
**<u>要先把ssh公钥添加到想要使用的代码托管平台后才能使用</u>**

![](img/pull&push.png)

<u>**下图所示相当于直接把远程仓库克隆到本地**</u>

<u></u>![](img/本地仓库与远程仓库连接.png)

<u>**下图指的是把本地已有的一个本地仓库与一个远程仓库连接，并且一个本地仓库可以与多个远程仓库（Github,Gitee,Gitlab皆可）连接，用git remote -v可以查看当前本地仓库与哪些远程仓库连接了**</u>

添加远程仓库！！！(step1和step2之间还差了一步：git branch -M main)！！！！
这里的远程仓库别名一般是origin（默认）

![](img/添加远程仓库.png)

## 三、其他用到的Linux、vim等指令

cat <fileName> ：可以查看所选文件的内容
echo  (作用很多，可以用于创建文件且向文件中写入信息，也可用于把文件添加进文件夹？)
vi <fileName>：用于修改文件

code . ：可用vscode打开当前目录下的文件

## 四、常用代码托管应用（远程仓库）

1.github
2.gitee(码云)：国内，访问快
3.gitlab(极狐)：可私有化部署

这三者的使用方式差不多

## 五、在Vscode中操作git

![](img/Vscode中操作git.png)