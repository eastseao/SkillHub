# SkillHub

> 来自 [eastseao/SkillHub](https://github.com/eastseao/SkillHub) 的 AI Skills 集合
>
> 一站式覆盖 AI Agent 学习、SEO、内容创作（公众号/小说/知乎）等多个场景。

---

## 📂 目录结构总览

```
SkillHub/
├── Agent Learning/      # AI Agent 学习路径（12 个子技能）
├── SEO/                 # 中文搜索引擎矩阵
├── novel/               # 小说创作工具集
├── wechat/              # 微信公众号全流程工具（10 个技能）
└── zhihu/               # 知乎网文工业化系统
```

---

## 🧠 Agent Learning（AI Agent 学习路径）

系统化学习 AI Agent 开发的 12 个阶段，从概念入门到项目生成、调试、案例积累。

| 序号 | 技能名称                   | 简介                 |
| :--: | -------------------------- | -------------------- |
|  01  | agent_concept_trainer      | Agent 核心概念训练师 |
|  02  | prompt_engineering_trainer | Prompt 工程训练师    |
|  03  | memory_architect           | 记忆架构师           |
|  04  | tool_use_master            | 工具使用大师         |
|  05  | workflow_designer          | 工作流设计师         |
|  06  | rag_knowledge_builder      | RAG 知识库构建器     |
|  07  | multi_agent_simulator      | 多智能体模拟器       |
|  08  | autonomous_agent_lab       | 自主 Agent 实验室    |
|  09  | agent_project_generator    | Agent 项目生成器     |
|  10  | agent_debugger             | Agent 调试器         |
|  11  | agent_case_library         | Agent 案例库         |
|  12  | daily_agent_trainer        | 日常 Agent 训练师    |

> 通用结构：`SKILL.md` + `config.yaml` + `prompts/` + `Memory/`（部分）

---

## 🔍 SEO（中文搜索矩阵引擎）

| 技能名称                   | 简介                                                         |
| -------------------------- | ------------------------------------------------------------ |
| **CNSearchMatrixEngineV6** | 多引擎聚合搜索系统，集成国内主流搜索引擎，支持高级搜索语法、时间筛选、站内搜索、隐私引擎及 WolframAlpha 知识查询 |

> 结构：`skill.md` + `config.yaml` + `prompts/` + `templates/` + `outputs/` + `memory/`

---

## ✍️ novel（小说创作工具集）

| 技能名称                  | 简介                                                         |
| ------------------------- | ------------------------------------------------------------ |
| **StorySeedGenerator**    | 故事种子生成器，快速搭建小说世界观、人物、情节骨架           |
| **deaify**                | 深度去AI化——彻底消除 AI 生成文本的"机器味"，让内容更像真人写作 |
| **novel-literary-master** | 网文文学大师，提供高质量网文写作辅助                         |
| **novel_factory**         | 小说工厂，批量生成小说内容                                   |
| **viral-webnovel-writer** | 爆款网文写手，捕捉热点、生成高传播网文                       |

> 安装：`npx skills add eastseao/skillhub@viral-webnovel-writer` 等

---

## 📣 wechat（微信公众号 AI 内容创作全流程）

覆盖公众号运营从选题到发布的完整链路，共 10 个技能。

| 序号 | 技能名称                            | 功能简介                                                     | 触发示例                    |
| :--: | ----------------------------------- | ------------------------------------------------------------ | --------------------------- |
|  1   | deep-digest                         | 深度解读——支持 PDF / 网页 / DOCX / 公众号文章 / YouTube 等多源内容的结构化摘要生成 | `深度解读这篇PDF`           |
|  2   | wechat-basic-formatting             | 将 Markdown 渲染为公众号样式 HTML，一键推送草稿箱（Node.js 18+） | `把这篇文章推到公众号`      |
|  3   | wechat-advanced-formatting          | 专业级排版——AI 辅助渲染、MPEC.md 格式、多种输出模式          | `高级排版`                  |
|  4   | wechat-all-in-one-viral-engine      | 爆款文全流程引擎——选题、标题(10~20个)、大纲、正文、AI 原创改写、封面图 | `生成一篇爆款文章`          |
|  5   | wechat-collect-7days-viral-articles | 提取近 N 天高阅读量公众号文章，可设最低阅读量阈值            | `收集7天内的爆文`           |
|  6   | wechat-operation-toolkit            | 公众号工具包——搜索、下载、AI洗稿改写、发布四大功能集成       | `搜公众号文章` / `帮我洗稿` |
|  7   | wechat-viral-writer                 | 爆款标题生成器 + 热点选题 + 原创/洗稿重写 + 情绪驱动内容增强 | `生成爆款标题`              |
|  8   | wechat-auto-publish                 | 将现成文章直接发布到公众号草稿箱（基于微信公众号 API）       | `发布到草稿箱`              |
|  9   | deaify                              | 深度去AI化——去除 AI "机器痕迹"，让内容更像真实人类写作       | `去AI味` / `人性化改写`     |
|  10  | novel-engine                        | 单部长篇小说连载生成系统——稳定世界观 + 爽点持续 + 防崩结构，支持百万字扩展 | `生成小说章节`              |

> **依赖环境：** Node.js（basic/advanced formatting、operation-toolkit、auto-publish）、Python（deep-digest、collect、viral-writer、all-in-one-viral-engine、deaify、novel-engine）

---

## 💬 zhihu（知乎网文工业化系统）

网文工业化生产系统，10+ 引擎模块化协作，覆盖从选题分析到完稿全流程。

| 序号 | 模块名称         | 简介                                 |
| :--: | ---------------- | ------------------------------------ |
|  01  | salt_analyzer    | 盐值分析器——评估内容吸引力与读者粘性 |
|  02  | hook_engine      | 钩子引擎——生成强吸引力开篇           |
|  03  | character_engine | 人物引擎——塑造立体角色               |
|  04  | emotion_engine   | 情绪引擎——驱动读者情感共鸣           |
|  05  | outline_engine   | 大纲引擎——规划故事结构               |
|  06  | rebuild_engine   | 重建引擎——改写与优化                 |
|  07  | chapter_engine   | 章节引擎——逐章生成正文               |
|  08  | title_engine     | 标题引擎——生成高点击标题             |
|  09  | style_engine     | 风格引擎——统一文风与调性             |
|  10  | database_engine  | 数据库引擎——素材管理与积累           |

> 含 `shared_knowledge/` 共享知识库目录

---

## 🚀 快速安装（通过 SkillHub CLI）

```bash
# 方式一：一键安装整套 wechat 技能包
npx skillhub install eastseao/skillhub

# 方式二：按需安装单个技能
npx skills add eastseao/skillhub@wechat-basic-formatting
npx skills add eastseao/skillhub@wechat-viral-writer
npx skills add eastseao/skillhub@deaify
npx skills add eastseao/skillhub@novel-engine
npx skills add eastseao/skillhub@viral-webnovel-writer
# 其他技能同理，按需替换 @ 后面的名称即可
```

---

## 📦 环境依赖速查

| 技能分类                            | 依赖环境                     |
| ----------------------------------- | ---------------------------- |
| wechat-basic-formatting             | Node.js 18+                  |
| wechat-advanced-formatting          | Node.js（见各 package.json） |
| wechat-operation-toolkit            | Node.js，npm install cheerio |
| wechat-auto-publish                 | bash, curl, jq               |
| deep-digest                         | Python 环境                  |
| wechat-collect-7days-viral-articles | Python 环境                  |
| wechat-viral-writer                 | Python 环境                  |
| wechat-all-in-one-viral-engine      | Python 环境                  |
| deaify                              | Python 环境                  |
| novel-engine                        | Python 环境                  |

---

## 📌 目录对应关系（本仓库 → GitHub 源码）

| 本地目录          | GitHub 路径       |
| ----------------- | ----------------- |
| `Agent Learning/` | `Agent Learning/` |
| `SEO/`            | `SEO/`            |
| `novel/`          | `novel/`          |
| `wechat/`         | `wechat/`         |
| `zhihu/`          | `zhihu/`          |

---

> 📂 源码：[https://github.com/eastseao/SkillHub](https://github.com/eastseao/SkillHub)
