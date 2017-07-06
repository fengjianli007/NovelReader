# NovelReader

仿照"任阅"的追书App。(目前感觉最重要贡献，就是重写了阅读器 0 0)

详见原作者项目地址:[任阅](https://github.com/JustWayward/BookReader)

# 应用简介

相对于原作增加的功能与修改:

1. 代码的逻辑优化，删除冗余代码
2. 采用数据库对数据进行存储。 (原作者是采用ACache类将数据修改成文本存储)
3. 增加书本的断点续传功能
4. 重写了小说的阅读页面 (风格模仿的是IReader)

注:原作部分功能还未实现，且有大量未知bug，正在慢慢完善中。。。

# 采用了以下开源框架

* [butterknife](https://github.com/JakeWharton/butterknife)    ==>    View注入
* [rxandroid](https://github.com/ReactiveX/RxAndroid)
* [rxjava](https://github.com/ReactiveX/RxJava)
* [greenDAO](https://github.com/greenrobot/greenDAO)    ==>    数据库
* [retrofit](https://github.com/square/retrofit)  ==> 网络
* [Glide](https://github.com/bumptech/glide)    ==>    图片加载
* [retrolambda](https://github.com/orfjackal/retrolambda)    ==>    在AndroidStudio3.0以下版本支持Lambda
* [treader](https://github.com/PeachBlossom/treader)    ==>    小说阅读页面的切换动画及整体架构都来自这个项目。
* [AndroidTagGroup](https://github.com/2dxgujun/AndroidTagGroup)    ==>    标签效果
# 应用展示

![](https://github.com/newbiechen1024/NovelReader/blob/master/screenshot/download.gif)

![](https://github.com/newbiechen1024/NovelReader/blob/master/screenshot/reader.gif)

![](https://github.com/newbiechen1024/NovelReader/blob/master/screenshot/load_local_file.gif)

# 更新记录

**update 2017-07-06**

更新(如果之前已安装过，需要卸载重新安装):
* 提供进入更新书本功能和按照阅读循序排序功能
* 提供加载阅读本地书籍功能。
* 提供加入、删除本地书籍功能。
* 修改了页面加载器的设计。
* 优化了加载章节的逻辑和数据库存取逻辑
* 优化页面的绘制逻辑

缺陷及未完成部分(由于这几天要复习，所以就先做到这里，过几天修复):
* 未提供书籍的预加载功能
* 本地加载的分页、分章算法有待优化(大文件耗时较长，内存占用较多),正则匹配章节名的数量不够准确
* 本地书籍加载的文件系统，暂时不支持删除文件功能，还有部分逻辑有bug
* 异常处理及特殊bug(代码写的不够健壮，如果发现问题，请及时提出)
* 页面加载类的设计有些乱。

**update 2017-06-07**
* 增加搜索书籍界面
* 增加阅读界面中小说目录中选择具体章节的用户体验(如增加滑动条，保证当前目录位置为正在阅读的小说章节的位置)
* 增加阅读界面中更多设置界面(提供音量键翻页，全屏显示效果)

**update 2017-05-30**

重构阅读页面逻辑(PageFactory类被弃用，提供了另一种加载方式，可用来学习)。
 * 增加对无网，弱网环境下的处理
 * 将百分比显示进度改成页码的方式
 * 增加页码切换的进度条
 * 字体大小可调节

**update 2017-05-29**
 * 完成收藏页书籍删除功能
 * 完成选择本地书籍功能(暂不支持加入书架)
