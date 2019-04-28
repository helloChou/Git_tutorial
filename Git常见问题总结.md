#  Git常见问题总结

> （1）git push 错误：failed to push some refs to

当在github上在线修改或者直接在github上的库中添加了文件，但没有对本地库进行同步时，如果下次在本地库中有commit想从本地库push到远程github库中时就会出现push错误。

参考<https://blog.csdn.net/MBuger/article/details/70197532>的构图，出现这个问题的原因是

![1556424777618](assets/1556424777618.png)

解决办法：用pull将github上的库下载（pull）下来与本地库进行同步。

![1556424824565](assets/1556424824565.png)

然后再次用本地库push同步github上的远程库

![1556424842228](assets/1556424842228.png)

**解决办法：**

```c++
git pull origin master
git add (需要添加的文件)
git commit -m "(修改信息)
git push origin master
```

