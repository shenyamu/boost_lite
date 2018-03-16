# boost_lite
boost1.64版本裁剪，支持linux和Aix，总大小只有十几兆，提供了boost一些基本模块和regex库；
1.	库的支持，如：智能指针、正则表达式（regex）、字符串处理（string algo）、可变类型（any、variant）、foreach、assign、tuple等，后续也可持续补充，弥补了c++98标准特性的不足，且支持各个平台（window、linux、aix等），便于应用的快速开发；
2.	Boost官方的原始源码支持的库非常多，比较庞大，解压后占用了五百多兆的空间，故对它进行了人工裁剪，最终得到的目录占用空间只有十几兆。 Boost大多数功能都是以hpp头文件的形式提供给应用使用，无需编译成库，除了少数几个库，利用自带工具“b2  --show-libraries”可以查看。
本次提取的功能中只有regex正则表达式需要编译库；
