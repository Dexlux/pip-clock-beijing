# pip-clock-beijing

北京时间和时 PiP 悬浮时钟,可用于抢购场景。

## 功能

- **北京时间**: 使用 `Intl.DateTimeFormat` 指定 `Asia/Shanghai` 时区,与设备时区无关
- **网络对时校准**: 启动时自动从多个 API 源(淘宝/苏宁/worldtimeapi/timeapi)对时,取 RTT 最小的结果,计算设备偏移并补偿
- **PiP 小窗**: Canvas 通过 `captureStream()` 转为视频流,支持点击按钮进入画中画模式
- **毫秒显示**: 时间显示到毫秒精度,方便抢购卡点
- **粒子特效背景**: 使用 canvas 绘制粒子网络背景

## 使用方法

1. 打开页面,等待对时完成
2. 点击"进入小窗"按钮进入 PiP 模式
3. 时钟会悬浮在任何其他 App/网页之上

## 平台支持

- Chrome/Edge/Mac Safari: 完美支持
- iOS Safari: 切到其他 App 时,系统可能冻结后台 JS(PiP 画面可能停住)

## 本地测试

```bash
python3 -m http.server 8080
# 访问 http://localhost:8080
```

## 部署

GitHub Pages 自动部署: `https://dexlux.github.io/pip-clock-beijing/`
