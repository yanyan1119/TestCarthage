# TestCarthage

0x01、首先安装OSX套件管理器Homebrew

ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)" 



0x02、使用 Homebrew 进行安装Carthage 安装之前先对Homebrew进行更新一下 不然可能会安装到比较老版本的Carthage

brew update



0x03、Homebrew 安装Carthage

brew install carthage



 到这里已经把Carthage工具安装完毕 

 下面是开始使用Carthage工具管理包（Carthage 是由 Swift 语言写的，只支持动态框架，只支持 iOS8+。 目前只支持github 或者git 相关管理源的库）

0x04、添加 Cartfile 文件 写法可参数官方例子 （https://github.com/Carthage/Carthage/blob/master/Documentation/Artifacts.md）

        如：github "ReactiveCocoa/ReactiveCocoa" >= 2.3.1

0x05、再执行 carthage update ；在执行 carthage update 命令后会在根目录创建一个 Cartfile.resolved 文件，这个文件是生成后的依赖关系，不能修改，同时还会生成一个Carthage 文件夹 里面放的是编译好的.framework文件



Cartfile 文件用来标注你需要哪些依赖库，对应版本或者 Git 分支 (需要提交到 Git)
Cartfile.resolved 文件用来跟踪项目当前所用的依赖版本号，为了保持多端开发一致 (需要提交到 Git)
Carthage 文件夹用来存放依赖库的源文件和编译后的文件 (不需要提交到 Git)
0x06、把编译好的.framework 文件同时放到Bild Phases 下面的Link Binary With Libraries里和General 里的Embedded Binaries里

0x07、添加修改.gitignore文件  添加 Carthage作为忽然文件夹 



例子：https://github.com/yanyan1119/TestCarthage
