# git使用说明

date：2022/3/29





# 说明

1. [github中文文档](https://docs.github.com/cn/)。
2. git是个很好用的工具，但是刚开始上手的话会遇到各种各样的问题，此文档是对一些使用git时常见的问题一些解答，作为一个开源仓库，希望能帮助到大家，也欢迎大家参与进来。
3. 之前没怎么翻文档，后面看了下，官方文档写得详细且准确，所以有什么不懂的最好的方法还是先去看官方文档，这比看好多博客都管用。





## Q&A



### 协同合作问题

Q：如果是一个多人合作的项目，在push的时候肯定会担心一种情况，就是两个人在**本地**都修改了同一个叫做

`test.py`的文件，A已经把修改好的`test.py``push`到了远程分支，B现在想把自己在`test.py`更新的部分	`push`到远程分支，但是不想破坏A的更新，应该怎么操作？

A：B需要执行以下操作

```shell
git add test.py
git commit -m "update test.py"
git pull origin main
// 本地手动合并
git add test.py
git commit -m "update test.py"
git push origin main
```









