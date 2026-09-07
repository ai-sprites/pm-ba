# pm-ba

独立 PM / BA 角色：从简报产出结构完整、详略合适的 PRD、规范用户故事与可观察验收；局部迭代更新已有需求。

## 复制到 AI 聊天

把下面这段粘贴到当前项目的 AI 聊天，让 AI 读取手册、自行识别客户端并放置资源。

```text
请阅读 https://github.com/ai-sprites/pm-ba 的 README、接入手册和资源清单，将 sprite-pm-ba 接入当前项目，一并带上本职能力 sprite-pm-ba-requirements 的完整 Skill、工作流和模板。
请自行识别当前客户端及项目已有结构，使用同一明确版本的资源。角色正文、Skill 和模板原样完整拷贝，只适配必要的目录与客户端元数据格式，不重新概括、改写或删减内容，保留我的项目规则和自定义；其他专项 Skill 按我的明确请求或实际任务需要处理。
资料 host repo 和产物 repo/目录已明确的直接沿用，缺项合并用白话问一次，允许稍后配置。需要跨 Git 资料桥接时按手册自动补齐并告知我，不另外索取安装确认。
完成后核对实际文件与相对引用，说明采用版本、保存位置、如何调用，以及当前客户端确需我完成的加载步骤。只有聊天权限时先在本会话使用，明确没有写入项目；不能读取源文件时直接说明，不自行编一个替代版本。
```

**[详细接入手册](docs/installation.md)** 说明 AI 如何选择资源、识别客户端、放置文件、处理已有内容和验证结果。用户无需执行安装命令；资料位置会主动引导确认，也可稍后配置。

## 资源清单

本清单对应当前阅读的仓库版本，资源链接随该页面或 checkout 的版本变化。接入时先固定为一个完整 Git 提交，再读取该提交的同批资源。历史 **v0.2.0** 仍可明确选用，但内容以该标签为准。角色 MD 定义职责与清单，具体能力在 Skill 中；本职 Skill 默认随角色接入，完整保留其工作流、模板和相对目录。安装资源不等于生成所有业务文档。

| 资源 | 用途 | 接入范围 |
| --- | --- | --- |
| [templates/agent.md](templates/agent.md) | 职责、边界与交付检查清单 | 默认接入 |
| [skills/sprite-pm-ba-requirements/SKILL.md](skills/sprite-pm-ba-requirements/SKILL.md) | 本职能力入口 | 随角色默认完整接入 |
| [skills/sprite-pm-ba-requirements/assets/templates/prd.md](skills/sprite-pm-ba-requirements/assets/templates/prd.md) | 完整产物模板 | 随角色默认完整接入 |
| [skills/sprite-pm-ba-requirements/assets/templates/story.md](skills/sprite-pm-ba-requirements/assets/templates/story.md) | 完整产物模板 | 随角色默认完整接入 |
| [skills/sprite-pm-ba-requirements/references/workflow.md](skills/sprite-pm-ba-requirements/references/workflow.md) | 工作流与专业参考 | 随角色默认完整接入 |

本职能力由 `sprite-pm-ba-requirements` 提供，默认随角色接入，也可单独使用该 Skill。

接入、加载检查和用户需要完成的步骤统一见 [接入手册](docs/installation.md)，不复制成业务文档。

## 开始使用

完成接入后，直接向 AI 描述任务，例如：

> 请用 sprite-pm-ba，把这份功能简报整理到能交给团队评审的程度，保存到项目 docs/。待决定的问题直接问我。

这类任务默认交付一份结构完整、详略合适的 PRD，包含范围、规则、标准用户故事与验收，并给出实际文件链接。故事采用“作为……我希望……以便……”或项目已有的等价格式。PM 不会因为你催问产出，就自动制作设计稿、可点击原型或应用代码。

更新已有需求时，只修改受影响的规则、故事和验收，无须重新跑一遍完整流程。

客户端没有自动加载时，让 AI 先读取保存的角色文件或 Skill 入口。读取说明、写入项目和启动原生子代理是不同结果，按实际完成情况判断。

角色以当前请求和项目已有约定为依据；待确定项只影响依赖它的工作。可以从简报直接产出 PRD，也可以单独整理故事或更新一条规则，不要求其他角色先到场。

## 留存与交接

需要跨会话或跨项目复用时，直接让 AI 把需求正文、用户故事与验收保存到你指定的业务仓库/目录，或沿用项目已有位置，核对真实路径、依据和待确定项。已有文件优先；没有位置约定时可用 `docs/prd.md`（独立故事可放在 `docs/stories/<ID>-<name>.md`）。角色安装目录与业务产物目录分开。

角色可以自由组合；资料 host repo、版本和功能或文件由你指定，已有项目约定就沿用。当前任务确需跨 Git 读取、固定版本、比较或留存时，AI 会复用或按需补齐 artifact-bridge；普通本地资料和纯角色接入不安装它。目录、Git 与认证条件见 [产物交接说明](docs/artifact-handoff.md)。

## 后续维护

需要追加、更新或移除资源时，直接说明目标。AI 对照明确版本与现有文件比较，保留自定义，只处理指定范围；具体规则见 [手册](docs/installation.md#已有内容与后续维护)。
