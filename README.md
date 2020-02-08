# upload

### 解题思路：

- 原理基本文件上传实现（前端+后端）
- 拖拽上传，粘贴上传
- 大文件分片上传
- 断点续传
- 计算hash优化（web-worker、time-slice）
- 抽样hash (布隆过滤器)
- 请求并发数控制&重试
- 慢启动策略（碎片清理）

### 后续思考题：

1. requestIdleCallback兼容性，如何⾃⼰实现⼀个
web全栈架构师
  - 1. react也是⾃⼰写的调度逻辑，以后有机会写个⽂
  章介绍
  - 2. React⾃⼰实现的[requestIdleCallback](https://github.com/facebook/react/blob/master/packages/scheduler/src/forks/SchedulerHostConfig.default.js)
2. 并发+慢启动配合
3. 抽样hash+全量哈希+时间切⽚配合
4. ⼤⽂件切⽚下载
  * 1. ⼀样的切⽚逻辑，通过axios.head请求获取
  content-Length
  * 2. 使⽤http的Range这个header就可以切⽚下载
  了，其他逻辑和上传差不多
5. ⼩的体验优化
  * 1. ⽐如离开⻚⾯的提醒 等等⼩tips
6. 慢启动的变化应该更平滑，⽐如使⽤三⻆函数，把变
化率平滑的限制在0.5~1.5之间
7. websocket推送进度
8. ⽂件碎⽚分机器存储
9. ⽂件碎⽚备份
10. cdn


## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Run your tests
```
npm run test
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
