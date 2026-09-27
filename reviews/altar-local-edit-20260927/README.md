# 局部布置对照 · 2026-09-27

这些截图来自实际 T01 模型与 iPhone 场景的独立副本，使用 App 共用 AltarRuntime / canvasGestures，Chrome 414×896 pt、DPR 2。只展示三维画布，没有原生操作栏；不作为完整 UI 或 iPhone 性能验收。未回写用户场景或草稿。

| 图片 | 状态 |
| --- | --- |
| 01-overview.jpg | 进入前整体构图 |
| 02-local-plate.jpg | 果盘局部取景，为顶部信息和底部卡片预留空间 |
| 03-local-moved.jpg | 实际 pointer 拖动水果后，尺寸和相机不变 |
| 04-overview-comparison.jpg | 整体对照，精确恢复原相机 |
| 05-local-added.jpg | 通过原物件添加流程放入新水果 |
| 06-local-burning.jpg | 当前场景点燃效果开启 |
| 07-local-orbit.jpg | 空白旋转、双指缩放后，场景保存相机不变 |

验证：整体/局部十次切换未增加几何和贴图（34/26）；多选移动与双触点缩放回放通过，无运行时异常。测得的浏览器 draw + gl.finish 耗时只用于此环境回归，不能替代手机触摸延迟测量。
