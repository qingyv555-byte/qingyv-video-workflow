# Qingyv Video Workflow

一个公开的 Codex Skill：分析参考视频，并制作有表达力、可验证的动效视频。

A public Codex skill for analyzing reference videos and designing expressive, verifiable motion films.

## 视频对照 / Video comparison: Reconstruct

先看参考与复刻效果，再了解制作方法。复刻版对应原片前 **10 秒**，采用 Remotion 帧驱动动画。

Watch the reference and reconstruction first, then explore the workflow. The reconstruction covers the reference's first **10 seconds**, using frame-driven animation in Remotion.

### 参考视频 / Reference · 16.58 s

https://github.com/user-attachments/assets/c71ee897-e19b-4105-9ca2-db0e9918b848

### V3 复刻视频 / V3 reconstruction · 10 s

https://github.com/user-attachments/assets/53cad14d-2873-4bd6-a46f-f95f37c0f2a1

[原作来源 / Original source](https://v.douyin.com/qiuYNJbhRLY/) · [案例说明 / Case study](examples/link-04/README.md)

案例说明包含观看方法、改进与已知差异。花形拓扑、字体、网格透视与碎片曲线仍与参考不同。

The case study explains observation methods, improvements, and known differences. Flower topology, typography, grid perspective, and fragment motion curves still differ from the reference.

## 工作流 / Workflow

它把视频制作拆成一条可复用链路：

Video production follows a reusable sequence:

`产品用途 -> 表达动词 -> 起始状态 -> 动作过程 -> 结果落点 -> 下个镜头`

`Product purpose -> Expressive verb -> Initial state -> Motion -> Result -> Next shot`

核心能力 / Core capabilities:

- 每 0.5 秒图板建立全局镜头地图；快速段落按源帧率连续观察。<br>
  Build a shot map with timestamped contact sheets at 0.5-second intervals; inspect fast sequences at the source frame rate.
- 分开记录主体、辅助图层、文字、镜头、遮挡与声音。<br>
  Track subjects, supporting layers, text, camera motion, occlusion, and sound separately.
- 校准位移、画幅占比、旋转、形变极值、速度峰值与阅读停顿。<br>
  Calibrate displacement, screen coverage, rotation, deformation extremes, peak speed, and reading pauses.
- 用确定性的帧驱动代码制作，适用于 Remotion，也可迁移到其他时间线系统。<br>
  Use deterministic, frame-driven code in Remotion or adapt the method to other timeline systems.
- 用代表帧、密集转场图板、完整媒体检查和实际页面验证交付。<br>
  Validate representative frames, dense transition sheets, complete media files, and the final page integration.
- 用方向、执行蓝图和决策历史维持长任务连续性。<br>
  Preserve continuity with direction, execution blueprint, and decision-history documents.

## 安装 / Installation

Windows PowerShell:

```powershell
git clone https://github.com/qingyv555-byte/qingyv-video-workflow "$env:USERPROFILE\.codex\skills\qingyv-video-workflow"
```

如果目标目录已经存在，先在现有目录中执行 `git pull`，不要覆盖本地改动。

If the directory already contains a clone of this repository, run `git pull` there. Preserve any local changes.

## 使用 / Usage

在 Codex 中调用：

Invoke the skill in Codex:

```text
Use $qingyv-video-workflow to analyze this reference and design a verifiable motion-video workflow.
```

也可以直接描述任务，例如“按参考视频的节奏重做产品合集，先建立观察证据，再设计分镜并验证成片”。

You can also describe the task directly: "Rebuild a product reel with the reference's pacing. Gather observation evidence first, then design the shots and validate the finished film."

## 结构 / Repository guide

| 文件 / File | 中文说明 | English description |
| --- | --- | --- |
| `SKILL.md` | 入口、任务分流和不变约束 | Entry point, task routing, and core constraints |
| `references/observation.md` | 节省上下文的分层观看方法 | Layered observation with an efficient context budget |
| `references/motion-direction.md` | 表达、幅度、分轨与节奏 | Expression, amplitude, motion tracks, and pacing |
| `references/production-and-validation.md` | 实现、声音、渲染和验收 | Implementation, sound, rendering, and validation |
| `references/templates.md` | 可复制的工作表 | Reusable worksheets |
| `references/project-memory.md` | 长任务连续记忆 | Continuity across long tasks |
| `references/sources.md` | 方法来源与边界 | Sources and limitations |

## 适用边界 / Scope

这个 Skill 提供判断流程和验证方法，附有独立的视频对照案例，不包含私有项目资料或第三方预设，也不会自动授予发布和部署权限。不同项目仍需根据真实内容重新设计动作。

This skill provides a decision workflow, validation methods, and a video comparison case study. It includes no private project material or third-party presets and does not grant publishing or deployment permissions. Design motion around each project's actual content.

## 许可 / License

工作流文档和代码采用 MIT。示例参考视频及音轨等第三方素材不包含在 MIT 授权中，详见案例说明。

Workflow documentation and code use the MIT license. Third-party media, including the example reference video and soundtrack, are excluded from that license; see the case study for details.
