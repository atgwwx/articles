# seajs模块化原理

## 模块化定义API
模块化定义API，非常简单，主要包括：

* define(id？,deps？,factory):模块定义
	* factory: funciton(require, exports, module){}:模块定义函数对应三个参数
* seajs.use(id):模块调用

## 模块核心Module
module主要功能是模块定义、依赖管理、加载，状态标示

### Module六个状态

*  FETCHING: 1, // 1 - The `module.uri` is being fetched 
* SAVED: 2,// 2 - The meta data has been saved to cachedMods
*  LOADING: 3,// 3 - The `module.dependencies` are being loaded
* LOADED: 4,// 4 - The module are ready to execute 
* EXECUTING: 5,// 5 - The module is being executed
* EXECUTED: 6 // 6 - The `module.exports` is available

### Module主要方法
* load:加载依赖模块
* onload:依赖模块加载完成
* fetch:获取模块,会去加载js源文件
* exec:模块执行，factory函数执行

## seajs模块依赖执行顺序
seajs模块定义遵循CMD规范，举例说明seajsd模块加载顺序：
##### 情景
A依赖B,C,B依赖D

此时seajs.use('A'),seajs这是就会通过module.fetch将A的源文件加载过来，然后解析依赖，在调用module.load去加载依赖B,C,当加载完B的源文件解析依赖，又回去加载D模块，这时如果D模块加载完成，就会触发B模块加载完成，当B,C模块加载完成，就会触发A模块加载完成，当A模块加载完成，就会开始执行module.exec即factory函数，然后B.exec执行，D.exec执行，C.exec执行，最后通过A模块的exports对象暴露接口给调用者。