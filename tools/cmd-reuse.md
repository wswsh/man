其实所谓的复用技巧也只是我看网上的资料汇总出来的东西。只是很多没有单独拿出来介绍，总是和其他的一些技巧一并介绍。而我写的这篇只关注怎么用最简单的命令复用之前输入过的命令。

###### ！系列
网上的说法是，这些以！开始的标记（暂且就用标记来称呼吧）都是一些列特殊的环境变量。

**!! //上一条命令的全部内容**

	$cd test
	$echo !!
	cd test
**!^ //上条命令的第一个参数**

	$cd test
	$echo !^
	test
注意不是cd

**!$ //上条命令的最后一个参数**

	$cd first second last
	$echo !$
	last
**!* //上条命令的最后一个参数**

	$cd first second last
	$echo !$
	first second last
	
**!prefix //最近一条以prefix开始的命令**

注意这里的prefix可以是一个或者多个字母表
看了以上几条命令我只有感慨正则表达无处不在

**!prefix:p //打印但不执行最近一条以prefix开始的命令

###### ^系列

^foo		//上一条命令中去掉foo之后的命令    
^foo bar	//上一条命令中去掉foo和bar之后的命令  
^foo^bar	//上一条命令中把foo换成bar之后的命令  

###### 最后再说说其他的几个常用的：

cd - //回到上一次的目录  
cd ~//回到登入用户的home目录  
