##简介：
* XCode7制作iOS工程模板。
* XCode4.0的时候制作iOS工程模板还是很容易的，但是后来XCode去掉了空模板，而且模板制作变得没那么容易了。
* 官方的模板存放在（我使用的XCode7）目录/Applications/Xcode.app/Contents/Developer/Platforms/iPhoneOS.platform/Developer/Library/Xcode 下，有一个Templates文件夹，该文件夹里有File Templates（文件模板） 和 Project Templates（工程模板）两个子文件夹，你猜对了，Project Templates 就是我们要找的东西！
* 官方的iOS工程模板里面一个很重要的文件是TemplateInfo.plist，该文件以 xml 的格式配置模板。。（）感觉苹果自己是使用工具生成的）。。不管怎么说，已经这样了，那么就研究研究这些文件吧，照着其格式修修改改配置自己的自定义模板还是可行的，毕竟机制是一视同仁的！
* 具体的格式还是参考官方的TemplateInfo.plist，聪明的你还是可以蒙懂的哈^_^
* 或者参考这些文章吧： 
<br/><br/>[A minimal project template for Xcode 4](http://blog.boreal-kiss.net/2011/03/11/a-minimal-project-template-for-xcode-4/)
<br/><br/>[How to Create Custom Project Templates in Xcode 7](http://www.telerik.com/blogs/how-to-create-custom-project-templates-in-xcode-7#disqus_thread)
<br/><br/>[Add Empty Application Template Back](https://coderwall.com/p/wucjeq/add-empty-application-template-back)
<br/><br/>[How to create project templates in Xcode 4](http://stackoverflow.com/questions/15491826/how-to-create-project-templates-in-xcode-4)
<br/><br/>[Creating Custom Xcode 4 Project Templates](http://meandmark.com/blog/2011/12/creating-custom-xcode-4-project-templates/)
<br/><br/>[About XCode 4 Project Template (How To Create Custom Project Template)](https://snipt.net/yonishin/about-xcode-4-project-template/)
<br/><br/>[找回xcode6丢失的那些内容](http://www.xiaoxiaozi.com/2015/01/30/2495/?utm_source=tuicool&utm_medium=referral)

* 这里是我根据自己的需求制作的模板，仅供参考，拿走不谢。

##注意：
鉴于Apple之后可能会改动（而不告知XCode用户：即iOS开发人员），这些文件只做参考

##用法：
1. （不推荐）直接拷贝Project Templates里面的iOS文件覆盖原路径下的文件，说了可能会变动，所以不推荐。
2. 仅拷贝*Project Templates* -> *iOS* -> *GJS CustomTemplate* 这个文件夹即可，放到对应路径下的iOS文件夹下
3. 重启XCode，好了，顺利的话应该会看到自定义模板啦，如果你有自己的需求打开TemplateInfo.plist文件修修改改吧，祝君好运！
4. 通过模板创建了工程之后，好吧，好像还没完，如果你选择的是自定义的singleViewApplication，而又同时点选了Use Core Data，那么要遗憾的告诉你的是这里我没有好办法处理，你只能手动删除工程里的Main文件夹。。由于一些实现上的问题。。这里需要包涵一下
5. 另外，singleViewApplication里面的main.storyboard需要手动修改一下，将ViewController改为你自己的根视图。