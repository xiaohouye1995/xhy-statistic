# xhy-statistic
小侯爷的埋点统计库

## 安装
```
npm install xhy-statistic -S
```

## 使用
```js
// 引用
import XhyStatistic from 'xhy-statistic';

// 注册
window.xhyWebtracing = new XhyStatistic()

// 初始化
window.xhyWebtracing.init({
  requestUrl: 'http://xxxx/tracing', // 请求路径
  appName: 'xxx', // 应用名
  eventCenter: eventCenter, // taro监听事件，可选
  appType: 'taro', // 应用类型，可选
})

/**
 * 自定义事件
 * @param name 事件名
 * @param optionsObj 事件参数
 */
window.xhyWebtracing.event(name, optionsObj)
```

### 参数
返回参数-暂定
```json
{
  "appName": "", // 应用名
  "distinctId": "", // 浏览器用户标识
  "pagePath": "", // 页面路径
  "source": "", // 访问来源
  "supporter": "", // 浏览器
  "system": "", // 系统
  "systemVs":" ", // 系统版本
  "region":" ", // 省份
  "city": "" ,// 城市
  "eventInfo": {}, // 自定义事件对象
  "pageTimeSrc": "", // 停留页面
  "pageTime": "", // 停留时间
  "eventType":"", // 事件名 pv：页面访问量，loginSuccess：登录成功，pageBack：返回上一级，pageOut：登出
  "userId": "" // 登录用户id
}
```