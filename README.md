# Industry Performance Template

面向企业管理者、绩效负责人和 HRBP 的行业绩效模板生成 Skill。它结合企业所处行业、发展阶段、历史执行效果、新方向尝试意愿以及资源约束，生成可直接讨论和落地的结构化绩效方案。

[![Release](https://img.shields.io/badge/release-v2.1.0-1769aa)](https://github.com/Zhanghaoran-ai/industry-performance-template/releases/tag/v2.1.0)
[![Python](https://img.shields.io/badge/Python-3.10%2B-0b7f78)](#安装后验证)

## 核心能力

每次调用均按固定 0—6 章结构输出：

1. 文档说明与数据边界
2. 企业与行业上下文摘要
3. 行业业务目标执行示例
4. 公司目标—部门—关键岗位—指标关联地图
5. 指标与目标明细：公式、外部参考、企业目标、设定原因和执行要点
6. 公司绩效模板：权重、评分规则、考核周期和否决项
7. 来源清单、证据登记和待企业确认事项

## 支持行业

- 互联网与科技
- 制造业
- 零售与消费品
- 金融
- 医疗健康
- 物流与供应链
- 新能源
- 房地产与建筑
- 教育培训
- 智能机器人与具身智能
- 其他行业：使用通用指标框架并结合当次公开证据补充

## 直接安装

在 [Releases v2.1.0](https://github.com/Zhanghaoran-ai/industry-performance-template/releases/tag/v2.1.0) 下载：

- `industry-performance-template-skill-v2.1.0.zip`：推荐，适合多数环境
- `industry-performance-template-skill-v2.1.0.tar.gz`：适合 Linux/macOS
- `SHA256SUMS.txt`：用于核对文件完整性

将安装包解压到所用 Agent 产品支持的用户 Skill 目录。解压后目录应为：

```text
industry-performance-template/
├── SKILL.md
├── references/
├── schemas/
└── scripts/
```

不要只复制 `SKILL.md`；配套脚本、行业参考库和 schema 都是运行所需文件。

## 安装后验证

```bash
python3 <技能根目录>/industry-performance-template/scripts/validate_input.py --help
python3 <技能根目录>/industry-performance-template/scripts/run_quality_gates.py --help
```

脚本只使用 Python 标准库。公开安装包包含 39 个运行文件，并已通过 39 项单元测试、入口脚本烟测及解压安装测试。

## 典型调用示例

- “以智能机器人行业为例，为一家初创企业提供绩效指标体系案例和指标明细。”
- “结合公司当前业务阶段和上季度执行效果，制定年度绩效模板。”
- “把公司聚合业务数据套入制造业模板，并生成岗位指标关联地图。”
- “检查现有 KPI 是否存在只追数量、忽视质量或现金风险的问题。”

## 方法与质量门禁

- 外部行业参考与企业建议目标分开，不把行业候选数字直接当作企业承诺。
- 缺少企业聚合基线时，使用标准待补表达或明确的匿名情景假设，不编造真实公司目标。
- 外部量化基准需要来源正文、发布日期、适用范围和证据等级。
- 指标体系同时覆盖结果指标、过程指标与质量/安全/现金护栏。
- 最终报告必须通过输入、来源、内容、结构和载体回读门禁。

## 数据安全边界

Skill 不提供跨任务的企业或员工数据存储机制。默认只处理岗位或团队层面的聚合数据，不需要员工姓名、联系方式、证件、家庭信息等个人敏感信息。公开仓库和安装包不包含企业数据、员工数据、运行报告、来源核验凭证、缓存或临时文件。

## 示例产物

[中国智能机器人初创企业绩效指标关联地图](./china-robotics-performance-map-2026.html) 展示 5 个公司目标、8 类关键岗位、16 项核心指标，以及结果/过程/护栏三类指标关系。示例目标值属于匿名情景假设，正式使用前需结合企业聚合基线重新校准。

## 版本与校验

当前版本：`v2.1.0`

- ZIP SHA-256：`181f8d79a4da207f41d48907546b493d5c151923193765e38542412ecf226177`
- tar.gz SHA-256：`d294dbb5b8f7d1958ab19334c21619e3ea976c5207d899b21c13c2b31ddec740`
