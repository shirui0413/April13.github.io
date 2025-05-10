### 新建react工程

```
npx create-react-app react-demo
```



#### 环境介绍

node_modules: 非常大

Public: 入口

Src: 源码文件

Package.json: 依赖配置文件



### JSX语法

Javascript + xml语法

遇到<>按照html解析，遇到{} 按照js语法解析



### 组件 component 

组件的后缀可以是 js ，也可以是jsx

一个react 项目可由成千上万个组件组成



### props属性

组件的复用性

同一组件跟据props呈现出不同。

**父件定义好，传给子元素的，所以props不可以被修改**



#### State



#### react的生命周期（life circle)



```flow
st=>start: start
ed=>end: end
dtProps=>operation: getDefaultProps
itState=>operation: getInitialState
willMount=>operation: componentWillMount
render=>operation: render
render2=>operation: render
didMount=>operation: componentDidMount
onWorking=>parallel: 运行中
ifPropsChange=>inputoutput: when props changed
onPropsChanged=>operation: componentWillReceiveProps
ifStateChange=>inputoutput: when state changed
onStateChanged=>operation: shouldComponentUpdate
ifUnmount=>inputoutput: when unmount
UnMount=>operation: componentWillMount
shouldCompUpdate=>condition: shouldComponentUpdate
componentWillUpdate=>operation: componentWillUpdate
componentDidUpdate=>operation: componentDidUpdate


st->dtProps->itState->willMount->render->didMount->onWorking
onWorking(path1,left)->ifPropsChange->onPropsChanged->shouldCompUpdate
onWorking(path2,bottom)->ifStateChange->shouldCompUpdate
onWorking(path3,right)->ifUnmount->UnMount->ed
shouldCompUpdate(true)->componentWillUpdate->render2->componentDidUpdate
shouldCompUpdate(false)->onWorking





```

### React生命周期函数列表：

componentWillMount: 在组件渲染之前执行

componentDitMount: 在组件渲染之后执行

shouldComponentUpdate: 返回true或false，true代表允许改变，false代表不允许改变

componentWillUpdate: 数据在改变之前执行（state，props）

componentDidUpdate:  数据修改完成（state，props）

componentWillReceiveProps: Props发生改变执行

componentWillUnMount: 组件卸载前执行



















