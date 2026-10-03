# 链接4：Reconstruct 动效复刻案例 / Link 4: Motion reconstruction case study

本案例展示参考观察如何用于校准动态幅度与镜头内变化。参考文件约 16.58 秒，V3 只复刻其前 10 秒（30 fps、300 帧）；对照时使用共同的 0–10 秒范围。它仍是近似实现，不是逐像素复刻。

This case shows how observing a reference helps calibrate motion amplitude and changes within a shot. The reference is about 16.58 seconds; V3 reconstructs only its first 10 seconds (30 fps, 300 frames). Compare the shared 0–10-second range. The result is an approximation, not a pixel-exact reconstruction.

| 参考视频 / Reference | 复刻视频 / Reconstruction |
| --- | --- |
| [观看参考 / Watch reference MP4](reference.mp4) | [观看复刻 / Watch V3 MP4](reconstruction-v3.mp4) |

GitHub 文件页若不直接播放，可点击 View raw / Download 查看。

If a GitHub file page does not play the video inline, use View raw / Download.

## 来源与素材说明 / Source and media rights

参考来自抖音分享链接：[“Reconstruct”交织 仿纸神](https://v.douyin.com/qiuYNJbhRLY/)。参考文件保留用于对照，请以原发布页面为作者与作品信息依据；不把原作归为本项目原创。

The reference comes from this [Douyin post](https://v.douyin.com/qiuYNJbhRLY/), titled “Reconstruct”交织 仿纸神. The file is included for comparison. Consult the original post for creator and work details; the original is not claimed as this project's own work.

本仓库 MIT 许可适用于工作流文档和代码，不对参考视频、原作视觉内容及音轨授予再许可。复刻片的音轨沿用参考素材，也不包含在 MIT 授权中。

The repository's MIT license covers workflow documentation and code, not the reference video, original visual content, or soundtrack. The reconstruction uses the reference soundtrack, which is also excluded from MIT licensing.

## 观察与实现 / Observation and implementation

1. 每 0.5 秒的时间戳图板建立全局镜头地图。<br>
   Build a shot map with timestamped contact sheets at 0.5-second intervals.
2. 前 10 秒进一步按源帧率检查约 240 帧，拆成 20 张、每张 12 帧的图板。<br>
   Inspect about 240 source frames from the first 10 seconds in 20 sheets of 12 frames each.
3. 分别分析文字、碎片、花形内部曲线、网格、镜头与遮挡，记录起始、极值、转折、结束。<br>
   Analyze text, fragments, internal flower curves, grids, camera motion, and occlusion separately; record starts, extremes, turns, and ends.
4. 用 Remotion 的帧号驱动动画；借鉴逐属性时间线和曲线校准方法，不直接运行 GSAP、Anime.js 或 Theatre.js。<br>
   Drive animation with Remotion frame numbers, applying ideas from property-specific timelines and curve calibration without running GSAP, Anime.js, or Theatre.js.
5. 在相同时间点对照参考与成片，再检查完整视频的节奏和连续性。<br>
   Compare reference and output at matching timestamps, then review pacing and continuity across the entire film.

## V3 改进与边界 / V3 improvements and limitations

修正文字和碎片的纵向运动，调整文字宽度、片尾缩放、花形控制点和收缩时间。相比 V2，消除了多段三联画及网格画面长时间近似静止的问题。

V3 corrects vertical text and fragment motion and adjusts text width, ending scale, flower control points, and contraction timing. Compared with V2, it removes several extended, nearly static intervals in the triptych and grid shots.

既有验证：10 秒、300 帧，音轨与完整解码通过。静止检测仅检出开头 0–0.375 秒暗场；该指标不证明视觉和幅度已经匹配。

Existing validation confirms 10 seconds, 300 frames, an audio track, and successful full decoding. Static-interval detection found only the opening dark section at 0–0.375 seconds; this metric does not establish visual or amplitude accuracy.

已知差异：花形交错拓扑、字体、网格透视与纹理、金属遮挡、碎片形状及末端曲线仍与原片不同。这个案例用于展示方法及其局限，不能作为精准复刻的证明。

Known differences remain in flower topology, fonts, grid perspective and texture, metallic occlusion, fragment shapes, and ending motion curves. This case illustrates the workflow and its limitations; it is not evidence of an exact reconstruction.
