# 安装 webstorm
  1. 安装webstorm
  2. 将JetbrainsCrack-2.7-release-str.jar放到一个固定目录，
     比如：/Users/qinshuangchun/soft/intelijIdea/JetbrainsCrack-2.7-release-str.jar
  3. 使用文本编辑打开webstorm安装目录下的 webstorm.vmoptions 文件，
     路径可能为：/Applications/WebStorm.app/Contents/bin/webstorm.vmoptions
  4. 在文件最后添加一句： -javaagent:JetbrainsCrack-2.7-release-str.jar文件路径，
     比如： -javaagent:/Users/qinshuangchun/soft/intelijIdea/JetbrainsCrack-2.7-release-str.jar
  5. 复制如下文本：

        {"licenseId":"1337",
        "licenseeName":"qinscx",
        "assigneeName":"",
        "assigneeEmail":"",
        "licenseRestriction":"Unlimited license till end of the century.",
        "checkConcurrentUse":false,
        "products":[
        {"code":"II","paidUpTo":"2099-12-31"},
        {"code":"DM","paidUpTo":"2099-12-31"},
        {"code":"AC","paidUpTo":"2099-12-31"},
        {"code":"RS0","paidUpTo":"2099-12-31"},
        {"code":"WS","paidUpTo":"2099-12-31"},
        {"code":"DPN","paidUpTo":"2099-12-31"},
        {"code":"RC","paidUpTo":"2099-12-31"},
        {"code":"PS","paidUpTo":"2099-12-31"},
        {"code":"DC","paidUpTo":"2099-12-31"},
        {"code":"RM","paidUpTo":"2099-12-31"},
        {"code":"CL","paidUpTo":"2099-12-31"},
        {"code":"PC","paidUpTo":"2099-12-31"},
        {"code":"DB","paidUpTo":"2099-12-31"},
        {"code":"GO","paidUpTo":"2099-12-31"},
        {"code":"RD","paidUpTo":"2099-12-31"}
        ],
        "hash":"2911276/0",
        "gracePeriodDays":7,
        "autoProlongated":false}

  6. 启动webstorm，选择使用Activaction code激活，粘贴上面复制的内容，激活成功，正常打开webstorm

## 安装node.js环境
  1. 执行 brew install node 
  2. 安装的版本当前为 v8.7.0
  3. 执行 brew upgrade， node 升级至 

## 初始化 node 项目
node项目中，package.json 文件是必不可少的。我们可以使用 NPM 生成 package.json 文件，生成的文件包含了基本的结果：

    $ npm init
    This utility will walk you through creating a package.json file.
    It only covers the most common items, and tries to guess sensible defaults.

    See `npm help json` for definitive documentation on these fields
    and exactly what they do.

    Use `npm install <pkg> --save` afterwards to install a package and
    save it as a dependency in the package.json file.

    Press ^C at any time to quit.
    name: (node_modules) runoob                   # 模块名
    version: (1.0.0) 
    description: Node.js 测试模块(www.runoob.com)  # 描述
    entry point: (index.js) 
    test command: make test
    git repository: https://github.com/runoob/runoob.git  # Github 地址
    keywords: 
    author: 
    license: (ISC) 
    About to write to ……/node_modules/package.json:      # 生成地址

    {
    "name": "runoob",
    "version": "1.0.0",
    "description": "Node.js 测试模块(www.runoob.com)",
    ……
    }


    Is this ok? (yes) yes

以上的信息，你需要根据你自己的情况输入。在最后输入 "yes" 后会生成 package.json 文件。

Package.json 属性说明

    name - 包名。
    version - 包的版本号。
    description - 包的描述。
    homepage - 包的官网 url 。
    author - 包的作者姓名。
    contributors - 包的其他贡献者姓名。
    dependencies - 依赖包列表。如果依赖包没有安装，npm 会自动将依赖包安装在 node_module 目录下。
    repository - 包代码存放的地方的类型，可以是 git 或 svn，git 可在 Github 上。
    main - main 字段指定了程序的主入口文件，require('moduleName') 就会加载这个文件。这个字段的默认值是模块根目录下面的 index.js。
    keywords - 关键字

## cnpm
大家都知道国内直接使用 npm 的官方镜像是非常慢的，这里推荐使用淘宝 NPM 镜像。
可以使用淘宝定制的 cnpm (gzip 压缩支持) 命令行工具代替默认的 npm。
安装 cnpm：

    $ npm install -g cnpm --registry=https://registry.npm.taobao.org

安装完成之后就可以使用 cnpm 命令来安装模块了，使用 cnpm 命令，就是使用淘宝的镜像来安装模块。