# Qingyv Video Workflow

A public Codex skill for analyzing reference videos and designing expressive, verifiable motion films.

它把视频制作拆成一条可复用链路：

`产品用途 -> 表达动词 -> 起始状态 -> 动作过程 -> 结果落点 -> 下个镜头`

核心能力包括：

- 每 0.5 秒图板建立全局镜头地图；快速段落按源帧率连续观察。
- 分开记录主体、辅助图层、文字、镜头、遮挡与声音。
- 校准位移、画幅占比、旋转、形变极值、速度峰值与阅读停顿。
- 用确定性的帧驱动代码制作，适用于 Remotion，也可迁移到其他时间线系统。
- 用代表帧、密集转场图板、完整媒体检查和实际页面验证交付。
- 用方向、执行蓝图和决策历史维持长任务连续性。

## 视频对照案例

[链接4：Reconstruct 参考视频与 V3 复刻视频](examples/link-04/README.md)，附观看方法、改进和已知差异。

## 安装

Windows PowerShell：

```powershell
git clone https://github.com/qingyv555-byte/qingyv-video-workflow "$env:USERPROFILE\.codex\skills\qingyv-video-workflow"
```

如果目标目录已经存在，先在现有目录中执行 `git pull`，不要覆盖本地改动。

## 使用

在 Codex 中调用：

```text
Use $qingyv-video-workflow to analyze this reference and design a verifiable motion-video workflow.
```

也可以直接描述任务，例如“按参考视频的节奏重做产品合集，先建立观察证据，再设计分镜并验证成片”。

## 结构

- `SKILL.md`：入口、任务分流和不变约束。
- `references/observation.md`：节省上下文的分层观看方法。
- `references/motion-direction.md`：表达、幅度、分轨与节奏。
- `references/production-and-validation.md`：实现、声音、渲染和验收。
- `references/templates.md`：可复制的工作表。
- `references/project-memory.md`：长任务连续记忆。
- `references/sources.md`：方法来源与边界。

## 适用边界

这个 Skill 提供判断流程和验证方法，附有独立的视频对照案例，不包含私有项目资料或第三方预设，也不会自动授予发布和部署权限。不同项目仍需根据真实内容重新设计动作。

## License

工作流文档和代码采用 MIT。示例参考视频及音轨等第三方素材不包含在 MIT 授权中，详见案例说明。
