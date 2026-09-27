# 佛堂共用蜡烛效果

本批为实际发布模型的独立 Three.js 场景副本，不是手机完整 UI 截图。未点燃、旧版和新版使用同一相机、环境和固定相位，无新增 bloom。只发布图像和紧凑诊断数据，没有用户场景、草稿、数据库或模型文件。

## 对照

| 容器 | 未点燃 | 旧版 | 新版 |
| --- | --- | --- | --- |
| 玻璃灯罩 | [查看](glass-1-off-design.jpg) | [查看](glass-1-baseline-design.jpg) | [查看](glass-1-new-design.jpg) |
| 原始不透明灯座 | [查看](opaque-1-off-design.jpg) | [查看](opaque-1-baseline-design.jpg) | [查看](opaque-1-new-design.jpg) |
| 石钵放入蜡烛 | [查看](stone-1-off-design.jpg) | [查看](stone-1-baseline-design.jpg) | [查看](stone-1-new-design.jpg) |
| 金属材质参考 | [查看](metal-fixture-1-off-design.jpg) | [查看](metal-fixture-1-baseline-design.jpg) | [查看](metal-fixture-1-new-design.jpg) |
| 八支玻璃灯罩 | [查看](glass-8-off-design.jpg) | [查看](glass-8-baseline-design.jpg) | [查看](glass-8-new-design.jpg) |

metal-fixture 仅在独立验证场景中复制原材质并调整 metalness/roughness。资源名称不能决定真实材质；本次没有修改发布模型或为金属灯座写专用代码。

[8 秒动态视频](candle-lifecycle.mp4)：0.5 秒点燃，3–5 秒带容器移动，6.5 秒熄灭。30 fps 是证据视频采样率，不是 App 性能结论。另有各容器 near/far/top 图像。

## 检查结果与限制

- 全部蜡烛共用烛芯世界坐标、两批次火焰及八槽 PointLight。玻璃透射可见，实体墙遮挡通过；移除火焰几何后仍有明显周围照明。
- 1–8 支各有照明；超过八支保留全部火焰，挑选邻近/可见灯光。点燃、渐灭、移动、删除/同 ID 重建、固定缓冲检查通过。
- 33 图及视频无 shader/GL/运行时错误。模型材质不变；未新增全屏后处理或动态蜡烛阴影。不透明容器不会通过逐灯阴影阻断光的传播。
- 原生 iPhone 828×1792，19 节点场景副本补至八支：P50/P95 22.56/23.38 ms。先前密集 68 节点副本为 35.27/35.81 ms，超过 33.3 ms 目标；不能据此宣称所有场景稳定 30 fps。
- 原生计时是 JS 提交、GL 队列及完成同步的墙钟成本，不是独立 GPU 时间或屏幕 FPS。初始已有 1286 单独记录；测量中无新增错误。scene/saved/draft/camera 前后一致。
- 此为文本、像素及时序验证，不代替人工审美、完整 UI 或物理手指验收。

详细指标和固定相机见 graphics.json；原生结果见 native-final.json 与 native-comparison.json；源文件摘要见 manifest.json。
