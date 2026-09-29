# 宋子桓 · Zihuan Song

我写解释器、工程工具和后端服务，关注语言如何表达计算，以及系统如何保持可理解、可预测和可维护。

这里整理我的代码实验与工程实践。个人介绍、经历和文章见 [song-zh.com](https://song-zh.com)。

## 编程语言与解释器

从纸带上的指令执行，到作用域、对象模型，再到语言规则本身的可扩展性，这组项目记录了我对“语言应该如何设计”的持续追问。

### [BrainFuck Pro](https://github.com/SongZihuan/BrainFuckPro) · C

从一个很小的计算模型入手，把程序的执行过程展开来看。在 Brainfuck 解释器上加入扩展指令、断点和步进模式，也提供创建、检查和重置执行环境的 C API。

阅读入口：[执行环境与 API](https://github.com/SongZihuan/BrainFuckPro/blob/main/include/brainfuck.h) · [解释器实现](https://github.com/SongZihuan/BrainFuckPro/blob/main/src/brainfuck.c)

### [GWARF](https://github.com/SongZihuan/GWARF) · C

尝试自己组织一门语言的规则：控制流、作用域、函数、对象与异常。项目中保留了语法调整和修复记录，可以结合解析器、解释器与示例，观察语言机制如何落到实现中。

阅读入口：[解析器](https://github.com/SongZihuan/GWARF/tree/master/paser) · [解释器](https://github.com/SongZihuan/GWARF/tree/master/inter) · [示例程序](https://github.com/SongZihuan/GWARF/tree/master/demo)

### [VirtualMath](https://github.com/SongZihuan/VirtualMath) · C

进一步实验变量与表达式的关系。例如，`$10`、`$(20 + 30)` 这样的“超级变量”允许通过表达式访问变量，探索变量名超出普通标识符后的语言语义。代码分为核心解释器与使用它的交互程序。

阅读入口：[语法说明](https://github.com/SongZihuan/VirtualMath/blob/master/README.md) · [核心解释器](https://github.com/SongZihuan/VirtualMath/tree/master/vmcore)

### [VirMat](https://github.com/SongZihuan/VirMat-Program-Language) · C

对 VirtualMath 的一次深度重构，推翻了不少旧设计，两者不兼容。重新区分值本身与从属关系，组织变量空间、语句和解析规则。仓库主要留下了核心模型与解析器的头文件，是一次尚未完成的设计探索。

阅读入口：[值与从属关系](https://github.com/SongZihuan/VirMat-Program-Language/blob/main/src/vtc/value.h) · [变量空间](https://github.com/SongZihuan/VirMat-Program-Language/blob/main/src/vtc/var.h) · [解析器模型](https://github.com/SongZihuan/VirMat-Program-Language/blob/main/src/vtc/parser.h)

### [aFunlang](https://github.com/SongZihuan/aFunlang) · C++ / CMake

尝试用更少、更统一的基本规则组织语言，将可扩展字面量、控制结构函数化和运行时可塑性作为设计方向。README 记录了这些目标；现有代码可以从解析器、核心对象和运行时模块开始阅读，具体完成范围以实现为准。

阅读入口：[设计说明](https://github.com/SongZihuan/aFunlang/blob/main/README.md) · [解析器](https://github.com/SongZihuan/aFunlang/tree/main/src/parser) · [运行时](https://github.com/SongZihuan/aFunlang/tree/main/src/runtime)

这条探索路线包含多次重新设计。我愿意回头检验已有的假设，也在这些实验中逐渐明确：表达自由需要可以理解的规则，抽象需要能够解释的实现。

## 工程工具与基础设施

另一组项目来自服务部署和日常开发中的具体问题：依赖如何准备，配置如何加载，连接如何管理，程序如何启动和退出。

- **[BackendServerTemplate](https://github.com/SongZihuan/BackendServerTemplate) · Go**
  将日志、命令行、配置读取、配置变更后重启、服务注册与优雅退出组织成后端服务模板，探索一个服务从启动到清理的完整生命周期。阅读入口：[不同运行模式的入口实现](https://github.com/SongZihuan/BackendServerTemplate/tree/master/src/mainfunc)。

- **[CFEP](https://github.com/SongZihuan/CFEP) · CMake**
  在配置阶段下载、构建和安装第三方依赖，再交由 `find_package` 查找，处理构建前的依赖准备。阅读入口：[CMake 模块](https://github.com/SongZihuan/CFEP/tree/main/cmake/CMakeFindExternalProject)。

- **[ssh-watcher](https://github.com/SongZihuan/ssh-watcher) · Go**
  SSH 监听与转发服务，支持基于 IP 和地理位置的访问规则、PROXY protocol，以及邮件和企业微信告警。阅读入口：[连接与转发实现](https://github.com/SongZihuan/ssh-watcher/blob/master/src/sshserver/server.go) · [配置定义](https://github.com/SongZihuan/ssh-watcher/tree/master/src/config)。

- **[huan-gogs](https://github.com/SongZihuan/huan-gogs) · Go**
  基于 Gogs 的定制版本，围绕实际部署需求调整邮件与 TLS、权限、登录和仓库创建逻辑。阅读入口：[改动说明](https://github.com/SongZihuan/huan-gogs/blob/main/README.md)。

## 早期探索与项目状态

[CoTan](https://github.com/SongZihuan/CoTan) 是早期用 Python 探索科学计算、数据处理与工具集成的项目。更多实验保留在 [仓库列表](https://github.com/SongZihuan?tab=repositories) 中。

上面列出的项目均已归档，保留作历史作品与实验记录，不再持续维护。它们记录了当时的实现与取舍，部分设计并未完成；阅读和使用时，请结合各仓库的文档与源码判断。

## 联系与开源约定

[个人官网与博客](https://song-zh.com) · [联系页](https://song-zh.com/contact) · [work@song-zh.com](mailto:work@song-zh.com)

[开源策略](https://song-zh.com/opensource) · [安全策略](https://song-zh.com/opensource/security-policy) · [行为准则](https://song-zh.com/opensource/code-of-conduct)

各项目的许可条款以其仓库内的许可证为准；本 Profile 仓库使用 [MIT License](LICENSE)。安全问题请按安全策略通过邮件报告。
