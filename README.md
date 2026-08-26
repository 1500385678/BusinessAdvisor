# BusinessAdvisor

> 经营顾问 · 24-经营-Business 行业 Web 项目  
> 让每个经营者身边都有一位"稻盛和夫 + 一位精益运营专家 + 一位管理学家"。

## 项目定位

BusinessAdvisor 是张勇的"经营顾问"知识体系 Web 化项目,把已沉淀的 **7 大知识图谱 + 500+ 案例 + 50+ 工具 + 50+ 行业基准** 转成可查询的 Web 应用,提供"哲学 + 方法 + 案例"三件套讲解,以及经营诊断 / 精益方案 / 客户经营 / 数字化转型 / 团队方案等 AI 能力。

| 形态 | 场景 | 状态 |
| --- | --- | --- |
| 飞书 Agent | 工作中随问随答 | ✅ 已上线 |
| Web App(本仓库) | 经营者 / 管理者 / 精益工程师 | ⏳ 规划中 |
| 桌面端 / 小程序 / REST API | 远期 | 📋 待规划 |

## 技术栈(规划)

- **后端**:FastAPI(Python 3.11+)+ PostgreSQL
- **前端**:React 18 + Vite + TypeScript
- **数据**:Markdown 源文件 → JSON 资产层 → PostgreSQL
- **AI**:大模型三件套(哲学 / 方法 / 案例)生成
- **部署**:Docker Compose 一键启动,GitHub Actions CI/CD
- **数据迁移**:SQLite → PostgreSQL(Phase 0 末)

> 当前仓库仍处 Phase 0 起步(仅 `.gitignore`),源码 / 构建配置待 T2 提交最小骨架后落地。

## 目录结构

```
BusinessWeb/
├── README.md                        # 本文件
├── 项目开发计划.md                  # Phase 0-4 checkbox 跟踪器
├── 经营顾问开发架构与计划.md        # 主计划(立项 + 技术方案 + 阶段定义)
├── .gitignore                       # Python + Node + 通用
├── .plan/                           # 每日开发项 plan(临时,推完删)
│   └── YYYYMMDD.md
└── .Log/                            # 巡检报告
    └── 巡检-经营-YYYYMMDD.md
```

未来扩展(Phase 0/1 推进后):

```
├── .Workflow/                       # 项目工作流(.Workflow/00_项目工作流.md)
├── .Core/                           # 项目核心信息(.Core/01_项目核心信息.md)
├── backend/                         # FastAPI 源码
│   ├── app/
│   │   ├── main.py
│   │   ├── api/                     # /graph /case /tool 路由
│   │   ├── services/
│   │   └── models/
│   ├── data/                        # 资产层 JSON
│   └── tests/
├── frontend/                        # React + Vite
│   ├── src/
│   │   ├── pages/
│   │   ├── components/
│   │   └── api/
│   └── package.json
├── data/                            # 灌库脚本 + 迁移脚本
└── docker-compose.yml
```

## 巡检入口

每日 02:50 自动巡检,产出报告至 `.Log/巡检-经营-YYYYMMDD.md`。  
每日 03:50 自动开发,按昨日 T4 写入的 `.plan/YYYYYMMDD.md` 推进 1 个可入库小变更,完成后 push Gitee + GitHub。

- **巡检纪律**:5 项巡检项,记录项目状态 / 阻塞 / 下一步
- **开发纪律**:1 天 1 个 commit,简洁可入库,checkbox 即时勾选
- **commit 命名**:`plan:` / `inspect:` / `feat:` / `fix:` / `docs:` / `chore:` 前缀

## 阶段路线

| 阶段 | 周期 | 目标 | 进度 |
| --- | --- | --- | --- |
| **Phase 0** 资产盘点 | 1-2 周 | md → JSON / 知识图谱 / 案例库 / 工具库 / 行业基准 / SQLite→PG 迁移 | 1/8 |
| **Phase 1** MVP | 4-6 周 | FastAPI 骨架 + React 前端 + 核心案例 / 工具 + 飞书 OAuth | 0/7 |
| **Phase 2** 完整功能 | 8-12 周 | 经营诊断 / 精益方案 / 数字化成熟度 / 客户分群 / 团队方案 | 0/7 |
| **Phase 3** AI 智能化 | 4-8 周 | AI 三件套讲解 + AI 深度诊断 / 精益 / 数字化 / 客户 / 团队方案 | 0/6 |
| **Phase 4** 多端 + 商业化 | 远期 | 小程序 / 桌面端 / 数据看板 / ERP 对接 / 付费会员 | 0/6 |

详细任务见 `项目开发计划.md`;主计划见 `经营顾问开发架构与计划.md`。

## 已有资产(主计划 §1.3)

- 7 份知识图谱:经营哲学 / 运营管理 / 精益生产 / 客户经营 / 团队经营 / 数字化经营 / 全球化经营
- 500+ 经营案例 / 50+ 工具模板 / 50+ 行业基准
- SQLite 表结构(`data.db`)
- 飞书 Agent persona / skill 触发配置

## 变更记录

- 2026-08-27 03:50 扩 README 为可用版本:6 段(定位 / 技术栈 / 目录结构 / 巡检入口 / 阶段路线 / 变更记录),从 2 行 73 字节扩到约 70 行;勾选跨阶段基础设施"README 完整说明"。
- 2026-08-23 首版:单行项目简介。
