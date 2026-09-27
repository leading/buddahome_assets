# 清水、茶、贴壁与轻动态 · 2026-09-28

以下原图均为相同机位、相同灯光的独立比较。无效拼图已移除，以原图和视频为准。

| 容器 | 空 | 清水半满 | 清水满 | 茶半满 |
| --- | --- | --- | --- | --- |
| 石钵 | [图](stone-water-0-design.jpg) | [图](stone-water-55-design.jpg) | [图](stone-water-100-design.jpg) | [图](stone-tea-55-design.jpg) |
| 陶瓷杯 | [图](ceramic-water-0-design.jpg) | [图](ceramic-water-55-design.jpg) | [图](ceramic-water-100-design.jpg) | [图](ceramic-tea-55-design.jpg) |
| 玻璃杯 | [图](glass-water-0-design.jpg) | [图](glass-water-55-design.jpg) | [图](glass-water-100-design.jpg) | [图](glass-tea-55-design.jpg) |

茶杯的清水图用于旧存档类型兼容和通用材质验证，**App 茶杯没有加水按钮**，由茶壶倒茶。只有直接装水的容器显示加水；编辑清空也只针对直接选中的容器，供桌和组合不代理其后代。

- [12 秒水面慢动态](water-breathing.mp4)：正常水位不升降、不改变贴壁边缘，仅有微弱法线波光。两组周期约 8.6/12 秒；空闲水面 15 fps，交互不等待这个间隔。
- [14 秒杯口热汽参考](tea-steam.mp4) / [热汽静帧](tea-steam-active.jpg)：前四秒模拟持续热茶入杯，随后冷却消散。此片展示杯口效果，不包含整段茶壶姿态；生产接入由 PourStream 根据实际茶流触发。
- 近/远检查分别见 stone、ceramic、glass 的 water-55-near / far.jpg；几何与着色器检查记录在相应 JSON。

## 验证边界

图像来自独立浏览器 WebGL 场景，使用实际发布 GLB 和生产 LiquidVolume / TeaSteam / SmokeBatch / SmokePass，不是完整 App 截图或物理 iPhone GPU 验收。相机、视口、时间与资源版本记录在 JSON。图片检查只使用文本、像素/几何等方式；不以工具回传内嵌图片。视频编码已核对时长和方向，轻微变化可能受到压缩影响。

- 真机场景副本检查石钵和杯子低/半/满水位的 64 个贴壁采样点，最大偏差小于 0.003 mm（资产坐标）；数据未写回手机。
- 900 帧呼吸检查没有顶点上传或 shader 重编译；实际 iPhone 只读确认相位推进、66.67 ms 调度、几何版本与 scene/saved/draft 不变。
- 热汽最多 96 粒子、4 个近期热杯；单杯检查峰值 31。共享既有纹理与半分辨率通道，没有每杯渲染目标。清水不生汽，清空/删除会清理，后台时间会使旧热汽消散。
- 茶的玻璃吸收仍是有界内腔近似，水面呼吸是法线效果，不是自由液面或热力学模拟。没有 Bloom 或额外后期掩饰边缘。

所有图片和视频作为文件提交，只分享固定提交版本的 GitHub HTTPS URL。未上传场景存档、草稿、设备数据库或 Base64 内容。
