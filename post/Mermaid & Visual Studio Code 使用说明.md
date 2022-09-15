# Mermaid & Visual Studio Code 使用说明

Mermaid 插件可以让你在 VS Code 中使用 Markdown 画出 `时序图` `流程图` 与 `甘特图`。

## 需要安装的插件

- Markdown Preview Mermaid Support
- Markdown All in One

## 时序图

```mermaid
sequenceDiagram
  A 店铺 ->> 平台 : 录入免费线索
  平台 ->> B 店铺 : 推送线索
  B 店铺 ->> + 平台 : 申请查看线索
  平台 -x A 店铺 : 发送查看通知
  平台 -->> - B 店铺 : 返回线索信息
  B 店铺 ->> + 车主 : 联系咨询
  车主 -->> - B 店铺 : 反馈
  B 店铺 ->> 平台 : 评价（真 / 假）
  平台 ->> A 店铺 : 发送评价通知
  A 店铺 ->> 平台 : 确认评价
```

### 消息

- `->>` 实线箭头，表示发送消息。
- `-->>` 虚线箭头，表示响应消息。
- `-x` 实线箭头带 x，表示异步操作，无需等待响应。

```mermaid
sequenceDiagram
  A ->> B : 现在几点了？
  A -x B : 快点回答
  B -->> A : 晚上 10:45
```

### 激活框

- `->> +` 表示从消息接受方的时间线上标记一个时间段的开始。
- `->> -` 表示从消息放回方的时间线上标记一个时间段的结束。`

```mermaid
sequenceDiagram
  A ->> + B : 现在几点了？
  A -x B : 快点回答
  B -->> - A : 晚上 10:45
```

### 选择（alt）

TODO

### 循环（loop）

TODO

## 流程图

TODO

- nihc
- nihc
