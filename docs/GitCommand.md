# Git基本操作
## Git操作对象
> 1. workspace: 工作区
> 2. staging aera: 暂存区/缓存区
> 3. local repository: 版本库/本地仓库
> 4. remote repository: 远程仓库  

## git init: 初始化
```
% git init
```
1. 想要用git管理某仓库，cd到该文件夹中或者新建一个文件夹如repo再cd进去，执行`% git init`。  
2. 该操作生成一个.git文件夹，包含git管理信息，表明repo文件夹已受git管理。  
3. repo文件空间即工作区，而缓存区和本地仓库在.git中。工作区相对随意，我们随意更改。而本地仓库就管理相对严格，不是我们随意访问修改的。所以我们在工作区修改一个内容，就通过命令将修改添加到缓存区中，等我们认为此次修改都改好了，再通过命令将缓存区所有内容一起添加到本地仓库中。这也保证了本地仓库到完整性和安全性。

## git add: 将工作区的更改添加到缓存区
```
% git add README.txt //添加文件
% git add dir //添加目录
% git add . //添加当前目录下所有内容
```
## git commit: 将缓存区内容添加到本地仓库
```
% git commit //会打开编辑器要求输入提交信息
% git commit -m 'message' //message就是直接输入的提交信息
% git commit -a //不从缓存区提交，直接提交工作区的更改，也就是不用`% git add`
% gti commit -am 'message'  //上面二者结合
```
提交信息比如：这是第几次提交，为什么提交，提及时间等等我们想注释此次提交的说明。

## git clone: 克隆远程仓库到本地
```
% git clone [url] 
% git clone https://github.com/zhukuhn/zhukuhn.github.io  //举例，将zhukuhn.github.io远程仓库文件夹拷贝到当前目录下
% git clone https://github.com/zhukuhn/zhukuhn.github.io newreponame  //将拷贝的文件夹改名

```
1. 此命令是从远程拷贝到工作区。
2. 自动将远程仓库的所有分支和历史记录都复制到本地。

## git push: 上传到远程仓库
```
% git push <远程主机名> <本地分支名>:<远程分支名>
% git push <远程主机名> <分支名>  //本地分支和远程分支名相同
% git push origin master  //举例
% git push --force origin master  //本地分支和远程分支有差异时强制推送

```
1. 此命令是从本地仓库推送到远程仓库。
2. 远程主机名和分支等后面再述。  
3. push是将本地内容推送到远程仓库，却没有网址信息。这是因为`% git clone`已经和远程仓库建立联系，可以直接push。关于这种联系后面再述。

# branch：Git库分支

# Git其他操作

## git fetch: 获取远程代码库

## git pull: 下载远程代码

## git remote: 远程仓库的操作

