# My Skills

这是一个用于管理个人 Codex / ChatGPT Agent Skills 的仓库。每个子目录对应一个独立 Skill，可单独安装、使用和迭代。

## Skills

| Skill | 功能 | 调用示例 |
| --- | --- | --- |
| [daily-work-report](./daily-work-report/) | 将零散工作记录整理为可直接粘贴到飞书或企业微信的中文工作日报 | `$daily-work-report 根据以下记录生成今天的日报：……` |
| [project-resume-highlights](./project-resume-highlights/) | 扫描项目证据，生成真实且可在面试中展开的简历项目经历 | `$project-resume-highlights 扫描当前项目并生成简历亮点` |
| [open-source-contribution-coach](./open-source-contribution-coach/) | 筛选合适的开源项目与 Issue，协作实现、测试、提交 PR 并沉淀真实经历 | `$open-source-contribution-coach 根据我的技术栈寻找合适的开源 Issue` |

## 仓库结构

```text
my-skills/
├─ README.md
├─ daily-work-report/
│  ├─ SKILL.md
│  └─ agents/
│     └─ openai.yaml
├─ project-resume-highlights/
   ├─ SKILL.md
   ├─ agents/
   │  └─ openai.yaml
   ├─ references/
   │  └─ writing-rules.md
   └─ assets/
      └─ project-resume-template.md
└─ open-source-contribution-coach/
   ├─ SKILL.md
   ├─ agents/
   │  └─ openai.yaml
   └─ references/
      └─ rubrics-and-templates.md
```

## 安装

使用 Codex 的 Skill Installer 安装指定子目录：

```text
$skill-installer https://github.com/lyxnbclass/my-skills/tree/main/daily-work-report
$skill-installer https://github.com/lyxnbclass/my-skills/tree/main/project-resume-highlights
$skill-installer https://github.com/lyxnbclass/my-skills/tree/main/open-source-contribution-coach
```

也可以将 Skill 文件夹复制到个人 Skill 目录：

```text
~/.codex/skills/
```

安装后如果没有立即出现，请重启 Codex。

## 使用

显式调用：

```text
$daily-work-report 根据我今天的工作记录生成一份可直接发送的日报。
$project-resume-highlights 扫描当前项目并生成简历中的项目描述、主要工作和技术亮点。
$open-source-contribution-coach 根据我的技术栈、目标岗位和每周可投入时间，筛选合适的开源项目与 Issue。
```

当请求与 Skill 的 `description` 匹配时，Codex 也可以自动调用对应 Skill。

## 维护约定

- 一个 Skill 只解决一类任务。
- 每个 Skill 必须包含 `SKILL.md`。
- 详细参考资料按需放入 `references/`。
- 需要确定性执行时再添加 `scripts/`。
- 模板、图标等输出资源放入 `assets/`。
- Skill 文件夹内不重复创建仓库级 README；本文件统一介绍整个仓库。
