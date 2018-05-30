# WordBook
单词本
首先，我是第一次应用ContentProvider去实现代码，根据老师在课上的教学，我也在网上了解了一些实现的方法以及具体的功能介绍，
ContentProvider 封装了数据的跨进程传输，我们可以直接使用 getContentResolver() 拿到 ContentResolver 进行增删改查即可。
ContentProvider 以一个或多个表（与在关系型数据库中的表类似）的形式将数据呈现给外部应用。 行表示提供程序收集的某种数据类型的实例，
行中的每个列表示为实例收集的每条数据。在通过  ContentResolver 进行数据请求时（比如 contentResolver.insert(uri, contentValues);）
系统会检查指定 URI 的 authority 信息，然后将请求传递给注册监听这个 authority 的 ContentProvider 。
这个 ContentProvider 可以监听 URI 想要操作的内容。不得不说在网上了解到的信息让我更快的掌握了这个进程通信的应用。
再有，我了解到安卓可以长安进行复制，我就想是否可以让复制到剪贴板的单词直接被单词本读入然后直接在数据可中搜索然后翻译，
实现从页面上可以查询单西的功能，但实现起来并没有很容易，打开一个网页是我之前实验中所学习的，接下来就是读取剪切版的内容，
我在网上找到了实现方法，剪贴板上复制内容发生变化，集调用了剪贴板，将内容复制到剪贴板后。最终得以实现
