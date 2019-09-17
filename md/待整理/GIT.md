# GIT

### [GIT](https://www.liaoxuefeng.com/wiki/896043488029600/897013573512192)

##### 命令

##### git status

- 文件没有被追踪	

  - 

  ```cmd
  On branch master
  Your branch is up-to-date with 'origin/master'
  nothing to commit, working directory clean
  ```

- 文件被追踪，但没有提交

  - ```
    On branch master
    Changes not staged for commit:
      (use "git add <file>..." to update what will be committed)
      (use "git checkout -- <file>..." to discard changes in working directory)
     
    	modified:   learn_git.txt
    	modified:   readme.txt
     
    no changes added to commit (use "git add" and/or "git commit -a")
    ```

- 文件被追踪，提交成功

  - ```
    $ git status
    On branch master
    nothing to commit, working tree clean
    ```

##### git diff

- 查看文件在工作区和版本库里面的区别

### 注意事项

##### 删除

- 删除一个已经提交上去的文件，不仅要在工作区里面删除，也要通知版本库已经删除了这个文件

  ```unix
  $ git rm test.txt
  rm 'test.txt'
  
  $ git commit -m "remove test.txt"
  [master d46f35e] remove test.txt
   1 file changed, 1 deletion(-)
   delete mode 100644 test.txt
  ```

##### 连接库报错

- [详解](https://www.cnblogs.com/jpfss/p/8094005.html)

- testing result 

  - 首先在本地电脑生成一个秘钥（公秘，私密）

  - ```
    $ ssh-keygen -t rsa -C "youremail@example.com"
    ```

  - 然后在自己的github配置秘钥，一个github可以配置多个设备秘钥

  - 将本地库推送到github里

  - 1、用ssh方式推送始终会出现 connect time out

    2、直接用http的方式推送

    ```csharp
    git remote add origin**************
    fatal: remote origin already exists.（报错远程起源已经存在。）
    ```

    上网查了下，有很多小白遇到过这个问题，以下是网上摘取的解决办法，
     解决办法如下：

    ```csharp
    1、先输入 git remote rm origin
    2、再输入 git remote add origin**************
    ```

    这样就不会报错了！

    - 第二个问题

    ```bash
    git remote add origin******
    The authenticity of host 'github.com ' can't be established（无法建立主机“github.com”的真实性）
    ```

    这是由于你的git地址采用了ssh方式，切换为https方式即可，也可能是你的仓库地址不对，可以用命令先查看一下：

    ```undefined
     git remote -v
    ```

    如果跟你的github地址不一样，那就去你的github上复制一下仓库地址
     然后在终端中输入：

    ```cpp
    git remote set-url origin https://github.com/yourname/learngit.git (这个是你的复制的仓库地址)
    ```

    最后再push下就可以了！

    ```undefined
    git push origin master 
    ```































