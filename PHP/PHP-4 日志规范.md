# 「PHP 规范」PHP-4 日志规范

## 1. 日志规范

### 1.1 基本规范

- PSR-3 日志接口规范中定义了八个方法，分别用来记录 [RFC 5424](http://tools.ietf.org/html/rfc5424) 中定义的八个等级的日志：debug、 info、 notice、 warning、 error、 critical、 alert 以及 emergency 。

### 1.2 日志级别和含义

- emergency
    - 系统不可用
- alert
    - **必须** 立刻采取行动
    - 例如：在整个网站都垮掉了、数据库不可用了或者其他的情况下， **应该** 发送一条警报短信把你叫醒。
- critical
    - 紧急情况
    - 例如：程序组件不可用或者出现非预期的异常。
- error
    - 运行时出现的错误，不需要立刻采取行动，但必须记录下来以备检测。
- warning
    - 出现非错误性的异常。
    - 例如：使用了被弃用的API、错误地使用了API或者非预想的不必要错误。
- notice
    - 一般性重要的事件。
- info
    - 例如：用户登录和SQL记录。
- debug
    - debug 详情
