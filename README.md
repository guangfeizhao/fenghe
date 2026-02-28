# 风和投资分析框架 (FengHe Investment Analysis Plugin)

基于风和基金创始人胡猛的 **3C3D5M3T** 投资哲学，构建的系统化公司分析 Claude Code 插件。

## 安装

在 Claude Code 中运行：

```bash
/plugin install guangfeizhao/fenghe
```

或在项目 `.claude/settings.json` 中添加：

```json
{
  "plugins": [
    {
      "source": "github",
      "repo": "guangfeizhao/fenghe"
    }
  ]
}
```

## 理论体系概览

```
┌─────────────────────────────────────────────────────────┐
│                   风和投资体系全景                         │
├─────────────────────────────────────────────────────────┤
│                                                         │
│  3C 投资哲学（世界观）                                    │
│  ├── Cycle    周期：万物皆有周期，有起必有落               │
│  ├── Change   变化：投资是投资变化，不投完美               │
│  └── Certainty确定性：唯一标准，不追求最大回报             │
│                                                         │
│  3D 股价驱动力（分析框架）                                │
│  ├── D1 ROE内延：匀速跑，内生价值成长                     │
│  ├── D2 外延变化：变速跑，结构性/周期性拐点 ──→ 用5M分析  │
│  └── D3 情绪估值：狗的驱动，市场非理性 ──→ 用3T理解       │
│                                                         │
│  5M 价值分析（微观工具）                                  │
│  ├── M1 目标市场  │ 做空侧重 ─┐                          │
│  ├── M2 市场份额  │ 做多侧重 ─┤                          │
│  ├── M3 利润率    │ 做多侧重 ─┤  围绕ROE拆解             │
│  ├── M4 商业模式  │ 做空侧重 ─┘                          │
│  └── M5 管理团队  │ 做多侧重                             │
│                                                         │
│  3T 时间框架（操作维度）                                  │
│  ├── T1  0-3月   最高确定性                              │
│  ├── T2  3-15月  中等确定性                              │
│  └── T3  15月+   最低确定性（已price in在估值中）         │
│                                                         │
│  LOGOS 风控系统（决策关卡）                               │
│  └── 100个风险排查点，<60分回锅                           │
│                                                         │
│  做空方法论                                              │
│  ├── 宴席理论：天下没有不散的宴席                         │
│  ├── 踩烂理论：已变烂的企业还会更烂                       │
│  ├── 结构性做空：M2份额蚕食                              │
│  └── 周期性做空：M3利润率见顶                             │
│                                                         │
│  组合构造                                                │
│  ├── 三低：低杠杆、低相关、低集中度                       │
│  ├── 止损：个股-12%，组合-2.5%砍20%头寸                  │
│  └── 盈利公式：HitRate×权重×回报 - 失败率×权重×亏损       │
│                                                         │
└─────────────────────────────────────────────────────────┘
```

## 包含的 Skills

| Skill | 功能 | 触发场景 |
|-------|------|---------|
| `fenghe-5m-analysis` | 5M价值分析框架 | 分析公司、评估企业价值、投资研究 |
| `fenghe-3c3d-framework` | 3C3D3T投资哲学 | 判断时机、估值、周期、确定性 |
| `fenghe-logos-risk-check` | LOGOS风险排查 | 投资决策前的风险检查 |
| `fenghe-long-short-thesis` | 多空投资论证 | 写投资报告、构建多空论据 |
| `fenghe-portfolio-construction` | 组合构造与风控 | 组合配置、仓位管理、风险控制 |

## 使用示例

### 分析一家公司

直接告诉 Claude：
```
帮我分析一下比亚迪
```

Claude 会自动使用 `fenghe-5m-analysis` skill 进行完整的5M分析。

### 风险检查

```
帮我做一下美的集团的LOGOS风险排查
```

### 多空论证

```
分析一下恒瑞医药的做多做空逻辑
```

### 组合审视

```
帮我检查一下我的持仓组合风险
```

## 插件结构

```
fenghe-analysis/
├── .claude-plugin/
│   └── plugin.json              # 插件清单
├── skills/
│   ├── fenghe-5m-analysis/      # 5M价值分析框架
│   │   └── SKILL.md
│   ├── fenghe-3c3d-framework/   # 3C3D3T哲学与驱动力
│   │   └── SKILL.md
│   ├── fenghe-logos-risk-check/ # LOGOS 100点风控
│   │   └── SKILL.md
│   ├── fenghe-long-short-thesis/ # 多空论证方法论
│   │   └── SKILL.md
│   └── fenghe-portfolio-construction/ # 组合构造与风控
│       └── SKILL.md
└── README.md
```

## 免责声明

本插件仅为投资分析辅助工具，不构成投资建议。所有投资决策应由具备资质的专业人士独立判断。AI生成的分析需经专业人员审核后方可参考。

---

*Based on "风和投资随笔" by 胡猛 (Hu Meng), Founder & CIO, FengHe Fund Management*
