# 小木审美 Skill

一个用于 PPT 审美训练、参考页拆解、页面诊断、风格统一检查和素材准入判断的 agent skill。

它不是 PPTX 生成器，也不是简单的“美化 PPT”提示词。它的目标是把优秀 PPT 的视觉经验拆成可观察、可复刻、可迁移、可审查的规则，并尽量落回 PowerPoint 原生操作。

## 适合场景

- 拆解 PPT 参考图为什么好看。
- 诊断一页 PPT 为什么丑、先改哪里。
- 检查一套 PPT 的风格是否统一。
- 判断图片、图标、背景、图表等素材能不能放进页面。
- 把优秀案例转成 wireframe、1:1 复刻任务和换内容迁移练习。

## 核心方法

- 先过内容结构门槛：页面任务、主信息、文案层级和信息关系不清时，不进入审美设计。
- 用审美金字塔判断当前页面层级：纯色、渐变、蒙版透明、创意组合。
- 用四维拆解参考图：样式、版式、配色、素材。
- 用 Design Spec 统一整套 PPT：主色、辅色、点缀色、字体、形状、图标、图片和背景。
- 用素材准入五问决定保留、压低、改造或删除。

## 安装

Codex：

```bash
git clone https://github.com/Liuguanyi2125/xiaomu-ppt-aesthetic-skill.git ~/.codex/skills/小木审美
```

Claude Code：

```bash
git clone https://github.com/Liuguanyi2125/xiaomu-ppt-aesthetic-skill.git ~/.claude/skills/小木审美
```

也可以把本仓库放进任意支持 `SKILL.md` 的 skills 目录。

## 文件结构

```text
SKILL.md
references/
  case-library-workflow.md
  diagnosis-template.md
  material-sop.md
  method-map.md
  style-spec-template.md
```

## 工作方式

- 不直接生成最终 PPTX。
- 如果需要完整 PPTX 生产，请把本 skill 输出的 Design Spec、素材结论和页面交接字段交给你自己的 PPTX 生成或演示文稿自动化工具。
- 视频理解是可选能力；如果使用课程视频或教程录屏，建议用 qwen3.6-plus 或同等级视频理解模型直接读取视频，不用固定间隔抽帧冒充理解。

## License

MIT
