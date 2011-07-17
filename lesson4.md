#lesson4_1笔记

akaedu@akaedu-desktop:~$ git clone git://github.com/happypeter/tg-note.git //克隆peter的笔记
Initialized empty Git repository in /home/akaedu/tg-note/.git/
remote: Counting objects: 81, done.
remote: Compressing objects: 100% (76/76), done.
remote: Total 81 (delta 24), reused 59 (delta 2)
Receiving objects: 100% (81/81), 7.67 KiB, done.
Resolving deltas: 100% (24/24), done.
akaedu@akaedu-desktop:~$ cd tg-note/
akaedu@akaedu-desktop:~/tg-note$ ls
note.md  README
akaedu@akaedu-desktop:~/tg-note$ vim note.md
akaedu@akaedu-desktop:~/tg-note$ vim note.md
akaedu@akaedu-desktop:~/tg-note$ cd
akaedu@akaedu-desktop:~$ cp tg-note/ my-note 
cp: 略过目录"tg-note/"
akaedu@akaedu-desktop:~$ cp tg-note my-note
cp: 略过目录"tg-note"
akaedu@akaedu-desktop:~$ cp tg-note my-note
cp: 略过目录"tg-note"
akaedu@akaedu-desktop:~$ cd tg-note/
akaedu@akaedu-desktop:~/tg-note$ cd
akaedu@akaedu-desktop:~$ cp -r tg-note/ my-note//重新复制一份 注意格式
akaedu@akaedu-desktop:~$ cp -r tg-note my-note
akaedu@akaedu-desktop:~$ cd my-note/
akaedu@akaedu-desktop:~/my-note$ ls
note.md  README
akaedu@akaedu-desktop:~/my-note$ vim note.md 
akaedu@akaedu-desktop:~/my-note$ markdown note.md >note.html // 用makrdown转换
akaedu@akaedu-desktop:~/my-note$ vim note.html
akaedu@akaedu-desktop:~/my-note$ firefox note.html //用火狐浏览器打开
akaedu@akaedu-desktop:~/my-note$ 

akaedu@akaedu-desktop:~/my-note$ git pull
github.com[0: 207.97.227.239]: errno=Connection timed out
fatal: unable to connect a socket (Connection timed out)

akaedu@akaedu-desktop:~/my-note$ tig
akaedu@akaedu-desktop:~/my-note$ rm -rf .git
akaedu@akaedu-desktop:~/my-note$ tig
akaedu@akaedu-desktop:~/my-note$ markdown note.md >note.html
akaedu@akaedu-desktop:~/my-note$ firefox note.html

tig: Not a git repository
akaedu@akaedu-desktop:~/my-note$ ls
note.html  note.md  README
akaedu@akaedu-desktop:~/my-note$ git init 
Initialized empty Git repository in /home/akaedu/my-note/.git/
akaedu@akaedu-desktop:~/my-note$ ls -a
.  ..  .git  note.html  note.md  README
akaedu@akaedu-desktop:~/my-note$ vim note.md
akaedu@akaedu-desktop:~/my-note$ ls
note.html  note.md  README
akaedu@akaedu-desktop:~/my-note$ git add note.md
akaedu@akaedu-desktop:~/my-note$ git commit -a -m "first version"

akaedu@akaedu-desktop:~/my-note$ tig
akaedu@akaedu-desktop:~/my-note$ vim note.md
akaedu@akaedu-desktop:~/my-note$ git commit -a -m "sec version"

1 files changed, 1 insertions(+), 1 deletions(-)
akaedu@akaedu-desktop:~/my-note$ tig
akaedu@akaedu-desktop:~/my-note$ 

// 上传
akaedu@akaedu-desktop:~/my-note$ git init
Initialized empty Git repository in /home/akaedu/my-note/.git/
akaedu@akaedu-desktop:~/my-note$ ls -a 
.  ..  .git  note.html  note.md  README
akaedu@akaedu-desktop:~/my-note$ git add note.md
akaedu@akaedu-desktop:~/my-note$ tig
tig: No revisions match the given arguments.
akaedu@akaedu-desktop:~/my-note$ git commit -a -m "psjicfh version"
[master (root-commit) f95a9f5] psjicfh version
 1 files changed, 176 insertions(+), 0 deletions(-)
 create mode 100644 note.md
akaedu@akaedu-desktop:~/my-note$ tig
akaedu@akaedu-desktop:~/my-note$ ls -a
.  ..  .git  note.html  note.md  README
akaedu@akaedu-desktop:~/my-note$ tig
akaedu@akaedu-desktop:~/my-note$ git remote add origin git@github.com:psjicfh/psjicfh-note.git
akaedu@akaedu-desktop:~/my-note$ git push -u origin master
The authenticity of host 'github.com (207.97.227.239)' can't be established.
RSA key fingerprint is 16:27:ac:a5:76:28:2d:36:63:1b:56:4d:eb:df:a6:48.
Are you sure you want to continue connecting (yes/no)? y
Please type 'yes' or 'no': yes
Warning: Permanently added 'github.com,207.97.227.239' (RSA) to the list of known hosts.
Counting objects: 3, done.
Delta compression using up to 2 threads.
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 1.37 KiB, done.
Total 3 (delta 0), reused 0 (delta 0)
To git@github.com:psjicfh/psjicfh-note.git
 * [new branch]      master -> master
Branch master set up to track remote branch master from origin.
akaedu@akaedu-desktop:~/my-note$ 




#lesson4_2 笔记

//账户密钥与锁
akaedu@akaedu-desktop:~$ ssh-keygen  //生成 ".ssh"文件夹
Generating public/private rsa key pair.
Enter file in which to save the key (/home/akaedu/.ssh/id_rsa): 
Created directory '/home/akaedu/.ssh'.
Enter passphrase (empty for no passphrase): 
Enter same passphrase again: 
Your identification has been saved in /home/akaedu/.ssh/id_rsa.
Your public key has been saved in /home/akaedu/.ssh/id_rsa.pub.
The key fingerprint is:
00:28:ee:6d:7f:b8:87:b0:fe:44:ab:74:2b:ed:a1:64 akaedu@akaedu-desktop
The key's randomart image is:
+--[ RSA 2048]----+
|   ..            |
|. .  .           |
|..    .          |
| .     .         |
|. .  .  S        |
| . +. .          |
|  .E==o          |
|  +o==oo         |
|  .++=+          |
+-----------------+
akaedu@akaedu-desktop:~$ cd .ssh //注意“cd ./文件夹名”打开同级文件夹  "cd .文件夹名"打开隐藏文件夹
akaedu@akaedu-desktop:~/.ssh$ ls
id_rsa  id_rsa.pub
akaedu@akaedu-desktop:~/.ssh$ 
akaedu@akaedu-desktop:~/.ssh$ vim id_rsa.pub //此时复制密钥

akaedu@akaedu-desktop:~/.ssh$ cd
akaedu@akaedu-desktop:~$ cd my-note/
akaedu@akaedu-desktop:~/my-note$ ls
note.html  note.md  README
akaedu@akaedu-desktop:~/my-note$ vim note.md
akaedu@akaedu-desktop:~/my-note$ vim note.md
akaedu@akaedu-desktop:~/my-note$ git config --global user.name "psjicfh"
akaedu@akaedu-desktop:~/my-note$ git config --global user.email psjicfh@yeah.net 
//变成自己的
akaedu@akaedu-desktop:~/my-note$ tig //但是此时进去后用户名还没变因为是以前保存的

akaedu@akaedu-desktop:~/my-note$ ls -a 
.  ..  .git  note.html  note.md  README
akaedu@akaedu-desktop:~/my-note$ rm -rf .git
akaedu@akaedu-desktop:~/my-note$ ls -a
.  ..  note.html  note.md  README
akaedu@akaedu-desktop:~/my-note$ tig
tig: Not a git repository
akaedu@akaedu-desktop:~/my-note$ git init
Initialized empty Git repository in /home/akaedu/my-note/.git/
akaedu@akaedu-desktop:~/my-note$ ls -a 
.  ..  .git  note.html  note.md  README
akaedu@akaedu-desktop:~/my-note$ tig
tig: No revisions match the given arguments.
akaedu@akaedu-desktop:~/my-note$ git add note.md
akaedu@akaedu-desktop:~/my-note$ git commit -a -m "psjicfh version"
[master (root-commit) a1f215e] psjicfh version
 1 files changed, 176 insertions(+), 0 deletions(-)
 create mode 100644 note.md
akaedu@akaedu-desktop:~/my-note$ tig
akaedu@akaedu-desktop:~/my-note$ tig
akaedu@akaedu-desktop:~/my-note$ vim note.md
akaedu@akaedu-desktop:~/my-note$ git commit -a -m "first version"
[master f5e238c] first version
 1 files changed, 1 insertions(+), 1 deletions(-)
akaedu@akaedu-desktop:~/my-note$ tig 
//此时已经改变成自己的用户了  注意：此时的 akaedu@akaedu-desktop:~/my-note$ rm -rf .git
//这句可无 因为在执行  akaedu@akaedu-desktop:~/my-note$ git init会覆盖


akaedu@akaedu-desktop:~/my-note$ git remote add origin git@github.com:psjicfh/psjicfh-note.git
akaedu@akaedu-desktop:~/my-note$ git push -u origin master
The authenticity of host 'github.com (207.97.227.239)' can't be established.
RSA key fingerprint is 16:27:ac:a5:76:28:2d:36:63:1b:56:4d:eb:df:a6:48.
Are you sure you want to continue connecting (yes/no)? y
Please type 'yes' or 'no': yes
Warning: Permanently added 'github.com,207.97.227.239' (RSA) to the list of known hosts.
Counting objects: 3, done.
Delta compression using up to 2 threads.
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 1.37 KiB, done.
Total 3 (delta 0), reused 0 (delta 0)
To git@github.com:psjicfh/psjicfh-note.git
 * [new branch]      master -> master
Branch master set up to track remote branch master from origin.
//到此上传成功

添加密钥：https://github.com/ -> Account Settings(右上) -> SSH Public Keys
新建工程：https://github.com/ -> New Repository (右中) -> 填写完第一 第二栏 -> Create Repository ->生成提示页面

//若将笔记修改想重新上传则：
psjicfh@ubuntu:~/my-note/lesson1$ git init
Reinitialized existing Git repository in /home/psjicfh/my-note/lesson1/.git/
psjicfh@ubuntu:~/my-note/lesson1$ git add lesson1.md
psjicfh@ubuntu:~/my-note/lesson1$ git commit -a -m "lesson1_2 version" //此时才重新生成“.git”
[master 78118bc] lesson1_2 version
 1 files changed, 1 insertions(+), 1 deletions(-)
psjicfh@ubuntu:~/my-note/lesson1$ ls -a
.  ..  .git  lesson1.md
psjicfh@ubuntu:~/my-note/lesson1$ tig //进去后可看见最新的 按“d”查看修改记录
psjicfh@ubuntu:~/my-note/lesson1$ git remote add origin git@github.com:psjicfh/lesson1.git
fatal: remote origin already exists. //致命错误：远程本已存在(因为此时是在覆盖)
psjicfh@ubuntu:~/my-note/lesson1$ git push -u origin master
Counting objects: 5, done.
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 299 bytes, done.
Total 3 (delta 1), reused 0 (delta 0)
To git@github.com:psjicfh/lesson1.git
   38db89b..78118bc  master -> master
Branch master set up to track remote branch master from origin.
psjicfh@ubuntu:~/my-note/lesson1$
//注：若不重新生成“.git”而是直接
psjicfh@ubuntu:~/my-note/lesson1$ git remote add origin git@github.com:psjicfh/lesson1.git
fatal: remote origin already exists.
psjicfh@ubuntu:~/my-note/lesson1$ git push -u origin master 则
Everything up-to-date //即：一切最新 因为没重新生成“.git”
