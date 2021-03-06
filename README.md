
<div align="center">
<img width="810" height="180" src="https://github.com/UCodeUStory/Relax/blob/master/source/relax.png"/>
</div>

<div align="center">

![Language](https://img.shields.io/badge/language-Kotlin-EE0000.svg)
![](https://img.shields.io/badge/QQ-1483888222-green.svg)
![SDK](https://img.shields.io/badge/SDK-14%2B-orange.svg)
[![License](https://img.shields.io/apm/l/vim-mode.svg)](https://github.com/UCodeUStory/Relax/tree/master/LICENSE)

</div>


Relax 基于Kotlin语言编写的一套组件化框架，内部可以实现灵活的配置

Relax is a android frame by Component Frame

### 语言
[Kotlin 解惑(>_<) 希望我踩过的坑对你有所帮助](https://github.com/UCodeUStory/Relax/tree/master/source/kotlin.md)


<div align="center">

<img width="180" height="320" src="https://github.com/UCodeUStory/Relax/blob/master/source/tianqi.jpg"/>
<img width="180" height="320" src="https://github.com/UCodeUStory/Relax/blob/master/source/meitu.jpg"/>
<img width="180" height="320" src="https://github.com/UCodeUStory/Relax/blob/master/source/xinwen.jpg"/>

</div>


### 架构模式

#### 1. module

      业务层，分解成独立的模块

      module-business-news   module-business-weather   module-business-welfare   module-business-four

      每个模块内部可以实现插件化跟细粒度小功能

#### 2. relax-business-component

      基础业务层，如地图封装、IM封装、日志上传封装、友盟统计封装、Bugly封装

#### 3. relax-data-component

      数据层，提供业务数据，包含网络数据、本地数据，SP数据

#### 4. relax-core-component

      基础组件层, 一些框架必须要用的library、核心的架构实现、如mvvm、mvp基础架构、自定义UI组件等

#### 5. relax-dependents

      公共依赖集合，提供统一配置

### 架构图

<div align="center">

<img width="1050" height="800" src="https://github.com/UCodeUStory/Relax/blob/master/source/new_frame.png"/>

</div>


### 项目内容

#### 1. 实现组件化，可以分层调试，单独模块调试；
#### 2. 支持 checkstyle,pmd,findBugs对代码静态扫描，虽然目前只支持Java检查，但开发过程中还是会用到一些Java代码和xml的检查；
#### 3. basic-component层 添加MVVM架构支持；
#### 4. basic-component层，添加MVP架构支持；
#### 5. 根据配置动态选择打包架构；
#### 6. 封装kotlin版本的权限检查，使用更简单；
#### 7. 将Application放到business-component层，因为我们要在这一层做基础业务组件开发，会全局初始化一些组件；
#### 8. 封装data层接口，对外通过DataServiceManager提供统一接口(LocalDataService和NetDataService)，在Service

      内部我们可以通过Retrofit、OkHttp、Volley等来实现网络请求,(项目核心使用rxjava来完成数据流，如果用其他网络框架，也尽量返回Observable,来保证封装一致性)

#### 9. 封装图片加载框架，通过ImageEngine对外提供加载图片引擎，通过ILoader对底层提供实现接口
#### 10. 封装插件化框架通过PluginManager进行管理插件

      例子：module-business-plugin模块就是用插件化实现的，具体插件式项目中的RelaxPluginDemo

### Library

1. [RxJava](https://github.com/ReactiveX/RxJava)
2. [Retrofit](https://github.com/square/retrofit)
3. [LifeCycle]()
4. [LiveData]()
5. [ViewModel]()
6. [ARouter](https://github.com/alibaba/ARouter)
7. [EventBus](http://greenrobot.org/eventbus/)
8. [Dagger](https://google.github.io/dagger/android)
9. [OKHttp](https://github.com/square/okhttp)
10. [GSON](https://github.com/google/gson)
11. [Glide](https://github.com/bumptech/glide)
12. [LeakCanary](https://github.com/square/leakcanary)
13. [Aspect](http://mvnrepository.com/artifact/org.aspectj/aspectjtools)



### 开发过程错误总结
- [错误日志](https://github.com/UCodeUStory/Relax/tree/master/source/error_note.md)







