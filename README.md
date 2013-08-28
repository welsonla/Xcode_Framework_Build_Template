Xcode_Framework_Build_Template
==============================

一个打包iOS Framework的模板


####编译环境
* Xcode 4.6
* SDK 6.1


####Note.
* 如果要变更framework的名字，请修改HelloFramework这个Taget的名字
* 编译输出选择iOS Device
* Target中的Compile Sources和Copy Headers中添加你要编译的文件，Copy Headers中文件移至Public


####Important Stemps
在Build Setting 中

* Base SDK选择Latest IOS(IOS 6.1)

* Build Active Architecture Only选择NO

* Dead Code Stripping设置为NO

* Mach-O Type 为Relocatable Object File

* Link With Standard Libraries为NO

* Wrapper Extension修改为：默认的bundle改成framework

* 在Architectures选项选择Standard(armv7 armv7s) (不这样编译会报错)

* 工程Info中将Bundle OS Type code的值BNDL改为：FMWK

* 打开Build Phases选项卡，右下角点击Add Build Phase–Add Headers copy，然后界面就会多出来一个Copy Headers的菜单，然后添加源文件

Thanks to:[http://www.cnblogs.com/qingjoin/p/3195720.html](http://www.cnblogs.com/qingjoin/p/3195720.html)
