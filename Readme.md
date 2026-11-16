# neo_uni
本项目是 [uni_legacy](https://github.com/Shyliuli/uni_legacy) 的手工重写版本，致力于在 loongarch 等平台上允许主程序加载异构动态库。

## WIP
下列项目作为本项目的模块正在开发或重写:
- [abi_plan](https://github.com/Shyliuli/abi-plan): 基于C签名生成对应ABI的寄存器与栈分配，用于对异构库函数调用。
## Plan
下列项目已在计划中:
- libbox64dl 库化box64以支持动态库接入和调用
- winedl 提供与libbox64dl相同的接口
- uni_stubgen 基于clang的头文件解析与abi_plan的能力，生成stub来避免显式代码修改
- unilib 完整的C ABI适配运行时环境
- uninode 完整的Node-API 插件适配运行时环境
## Goal
本项目的远期目标是允许主程序极小修改后即可加载闭源异构动态库(如x64 linux so与x64 windows dll)，并在此基础上实现对原生Node，Python，Java等调用异构插件的能力。
