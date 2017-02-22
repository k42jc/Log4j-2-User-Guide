#5 <span id="Configuration">Configuration</span>

##5.1 配置

在程序代码中插入日志请求需要相当多的努力和充分的准备，观察显示大约4%的代码是用于日志记录的。即时中等规模的项目也有成千上万行的日志语句，考虑到它们(众多)的数量，管理这些日志语句势在必行，而不是手动修改它们

以下4种方式都可以完成Log4j 2的配置：

1. 通过 XML, JSON, YAML, 或 properties 文件配置
2. 编程式，通过创建 ConfigurationFactory 和 Configuration 的具体实现
3. 编程式，通过调用API暴露 Configuration 接口添加组件到默认配置中去
4. 编程式，通过调用Logger类的内部方法

本页主要关注通过配置文件配置，编程式配置请参见[Extending Log4j 2章节](#Extending Log4j 2)以及[Programmatic Log4j Configuration.章节](#Programmatic Log4j Configuration)

注意，与1.x版本不同的是，公共Log4j 2的API没有暴露出增、删、改appender与filter或者操作配置的方法